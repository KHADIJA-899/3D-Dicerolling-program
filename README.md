# 3D-Dicerolling-program
# The Dice Rolling Game is a basic but effective Python project that demonstrates fundamental programming concepts. 
# It can be further enhanced by adding score tracking, multiplayer mode, or a GUI interface.

import random
import plotly.graph_objects as go
def roll_dice():
    return random.randint(1, 6), random.randint(1, 6)
    def show_dice(d1, d2):
    fig = go.Figure()

    # Dice 1 (3D cube position)
    fig.add_trace(go.Scatter3d(
        x=[0], y=[0], z=[0],
        mode='markers+text',
        marker=dict(size=50, color='red', symbol='square'),
        text=[f"Dice 1: {d1}"],
        textposition="top center"
    ))

    # Dice 2 (3D cube position)
    fig.add_trace(go.Scatter3d(
        x=[1], y=[1], z=[0],
        mode='markers+text',
        marker=dict(size=50, color='blue', symbol='square'),
        text=[f"Dice 2: {d2}"],
        textposition="top center"
    ))

    fig.update_layout(
        title="🎲 3D Dice Rolling Simulation",
        scene=dict(
            xaxis_title="X Axis",
            yaxis_title="Y Axis",
            zaxis_title="Z Axis"
        )
        while True:
    d1, d2 = roll_dice()

    print(f"\nYou rolled: {d1} and {d2} | Total = {d1 + d2}")

    show_dice(d1, d2)

    choice = input("Roll again? (yes/no): ").lower()
    if choice != "yes":
        print("Game Over 🎮")
        break
    )

    fig.show()
