# Cr-a-Th-rapie-Th-rapie-Artistique-Assist-e-par-IA
Créa-Thérapie utilise l'IA générative pour guider les patients dans des activités artistiques thérapeutiques personnalisées, favorisant l'expression émotionnelle et le bien-être mental.
import random

# A simple emotion to art activity mapping (for demonstration purposes)
emotion_to_activity = {
    "happy": ["paint a landscape that represents joy", "draw something that makes you smile"],
    "sad": ["create art using cool colors to express sadness", "sketch a scene that captures a melancholic mood"],
    "angry": ["use bold strokes to express anger", "draw something that frustrates you in abstract form"],
    "anxious": ["create a piece using circular patterns to calm anxiety", "sketch while focusing on your breath"],
}

# A list of follow-up questions to encourage reflection
reflection_questions = [
    "How do you feel after completing this activity?",
    "What emotions or thoughts arose during the process?",
    "Do you see a reflection of your current emotional state in your artwork?",
]

def generate_art_prompt(emotion):
    """Generate an art activity based on the user's current emotional state."""
    if emotion in emotion_to_activity:
        activity = random.choice(emotion_to_activity[emotion])
        print(f"Suggested Activity: {activity}")
    else:
        print("No activity found for the specified emotion. Try expressing how you feel freely through any form of art.")

def reflect_on_artwork():
    """Ask the user reflection questions to encourage emotional processing."""
    for question in reflection_questions:
        print(question)
        input("Your response: ")  # In a real app, responses would be saved and possibly analyzed

def main():
    print("Welcome to Créa-Thérapie: Your AI-Assisted Artistic Therapy Guide")
    
    # For demo, we directly specify an emotion. In a real scenario, this could be determined through a questionnaire or AI analysis.
    user_emotion = input("How are you feeling today? (happy, sad, angry, anxious): ")
    
    generate_art_prompt(user_emotion)
    reflect_on_artwork()

    # In a full application, there would be options to share the created art with a therapist or community, further AI analysis of the art, etc.

if __name__ == "__main__":
    main()
