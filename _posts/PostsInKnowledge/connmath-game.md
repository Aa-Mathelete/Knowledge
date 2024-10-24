---
title: Connected Math Game 7th Grade
tags: [Math, 7th Grade Stuff]
date: 10/24/24
---

import pygame
import time
import random

# Initialize Pygame
pygame.init()

# Set up display
WIDTH = 800
HEIGHT = 600
screen = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("Halloween Candyland")

# Colors
BLACK = (0, 0, 0)
WHITE = (255, 255, 255)
ORANGE = (255, 165, 0)
PURPLE = (128, 0, 128)

# Fonts
title_font = pygame.font.Font(None, 64)
text_font = pygame.font.Font(None, 32)

class GameState:
    START = "start"
    RULES = "rules"
    GAME = "game"
    MINIGAME = "minigame"

class Game:
    def __init__(self):
        self.state = GameState.START
        self.current_square = 0
        self.game_timer = 0
        self.game_started = False
        
        # Define board squares positions
        self.squares = [
            {"pos": (100, 300), "color": ORANGE},
            {"pos": (200, 200), "color": PURPLE},
            {"pos": (300, 300), "color": ORANGE},
            {"pos": (400, 200), "color": PURPLE},
            {"pos": (500, 300), "color": ORANGE},
            {"pos": (600, 200), "color": PURPLE},
            {"pos": (700, 300), "color": ORANGE},
        ]
        
        # Mini-games data
        self.minigames = [
            {"name": "Drive", "description": "Press SPACE repeatedly to drive!", "target": 10},
            {"name": "Parkour", "description": "Time your SPACE jumps perfectly!", "target": 5},
            {"name": "Run", "description": "Alternate SPACE presses to run!", "target": 8}
        ]
        self.current_minigame = None
        self.minigame_score = 0

    def draw_start_screen(self):
        screen.fill(BLACK)
        title = title_font.render("Halloween Candyland", True, ORANGE)
        instruction = text_font.render("Press SPACE to continue", True, WHITE)
        
        screen.blit(title, (WIDTH//2 - title.get_width()//2, HEIGHT//2 - 50))
        screen.blit(instruction, (WIDTH//2 - instruction.get_width()//2, HEIGHT//2 + 50))

    def draw_rules_screen(self):
        screen.fill(BLACK)
        rules = [
            "Welcome to Halloween Candyland!",
            "1. Move through the board by completing mini-games",
            "2. Each square triggers a different challenge",
            "3. Complete all mini-games to win",
            "Press SPACE to start the game"
        ]
        
        for i, rule in enumerate(rules):
            text = text_font.render(rule, True, WHITE)
            screen.blit(text, (WIDTH//2 - text.get_width()//2, 150 + i * 50))

    def draw_game_board(self):
        screen.fill(BLACK)
        
        # Draw connecting paths
        for i in range(len(self.squares) - 1):
            pygame.draw.line(screen, WHITE, 
                           self.squares[i]["pos"], 
                           self.squares[i + 1]["pos"], 3)
        
        # Draw squares
        for i, square in enumerate(self.squares):
            color = ORANGE if i <= self.current_square else WHITE
            pygame.draw.rect(screen, color, 
                           (square["pos"][0] - 20, square["pos"][1] - 20, 40, 40))
            
        # Draw timer if game has started
        if self.game_started:
            timer_text = text_font.render(f"Time: {int(self.game_timer)}s", True, WHITE)
            screen.blit(timer_text, (10, 10))

    def draw_minigame(self):
        screen.fill(BLACK)
        if self.current_minigame:
            title = text_font.render(self.current_minigame["name"], True, WHITE)
            description = text_font.render(self.current_minigame["description"], True, WHITE)
            score = text_font.render(f"Score: {self.minigame_score}/{self.current_minigame['target']}", True, WHITE)
            
            screen.blit(title, (WIDTH//2 - title.get_width()//2, HEIGHT//3))
            screen.blit(description, (WIDTH//2 - description.get_width()//2, HEIGHT//2))
            screen.blit(score, (WIDTH//2 - score.get_width()//2, 2*HEIGHT//3))

    def run(self):
        running = True
        clock = pygame.time.Clock()
        
        while running:
            for event in pygame.event.get():
                if event.type == pygame.QUIT:
                    running = False
                
                if event.type == pygame.KEYDOWN:
                    if event.key == pygame.K_SPACE:
                        if self.state == GameState.START:
                            self.state = GameState.RULES
                        elif self.state == GameState.RULES:
                            self.state = GameState.GAME
                            self.game_started = True
                            self.game_timer = 0
                        elif self.state == GameState.MINIGAME:
                            self.minigame_score += 1
                            if self.minigame_score >= self.current_minigame["target"]:
                                self.current_square += 1
                                self.state = GameState.GAME
                                self.current_minigame = None
                                self.minigame_score = 0
                                
                                if self.current_square >= len(self.squares):
                                    running = False  # Game won!

            # Update game timer
            if self.game_started and self.state != GameState.MINIGAME:
                self.game_timer += clock.get_time() / 1000
            
            # Handle clicking on squares
            if self.state == GameState.GAME:
                mouse_pos = pygame.mouse.get_pos()
                mouse_clicked = pygame.mouse.get_pressed()[0]
                
                if mouse_clicked:
                    for i, square in enumerate(self.squares):
                        square_rect = pygame.Rect(square["pos"][0] - 20, 
                                                square["pos"][1] - 20, 40, 40)
                        if square_rect.collidepoint(mouse_pos) and i == self.current_square:
                            self.state = GameState.MINIGAME
                            self.current_minigame = random.choice(self.minigames)
                            self.minigame_score = 0
            
            # Draw current state
            if self.state == GameState.START:
                self.draw_start_screen()
            elif self.state == GameState.RULES:
                self.draw_rules_screen()
            elif self.state == GameState.GAME:
                self.draw_game_board()
            elif self.state == GameState.MINIGAME:
                self.draw_minigame()
            
            pygame.display.flip()
            clock.tick(60)

        pygame.quit()

# Start the game
if __name__ == "__main__":
    game = Game()
    game.run()