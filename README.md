1. Language-Specific Challenges

Bengali has rich morphology, multiple dialects, and frequent code-mixing with English.

Preprocessing required normalization of spelling variations (e.g., “ভালো”, “ভাল”, “valo”).

Tokenization quality significantly affects fine-tuning because many Bengali words are subword-heavy.

2. Dataset Quality Matters the Most

Empathetic datasets require emotion-aligned responses, not only literal translations.

Utterances were manually checked to ensure cultural appropriateness in Bengali context.

Synthetic data augmentation (LLM-generated Bengali empathy dialogues) improved diversity.

3. Importance of Emotion Tags

For better empathy, emotion metadata such as:
{sadness, anxiety, anger, confusion, happiness, surprise, neutral}
was added to each training sample.
This helps the model produce more context-aware, human-like responses.

4. Safety Considerations

Extra safety prompts were added to ensure the model avoids harmful content.

The fine-tuned model was made more cautious in mental health–related conversations.

The training process avoided generating medical, legal, or abusive responses.

5. Training Infrastructure Notes

Mixed-precision (BF16/FP16) significantly reduced VRAM usage.

LoRA reduced parameter count and allowed training on a single GPU.

Gradient accumulation + low rank adaptation helped maintain stability even with small batch sizes.

6. Evaluation Approach

The model was evaluated using:

BLEU & ROUGE — for linguistic similarity

BERTScore — for semantic closeness

Human Evaluation — emotional correctness, gentleness, and clarity

Hallucination Rate — to ensure factual safety

7. Observations After Fine-Tuning

Clear improvement in context understanding for Bengali conversations.

Responses became more emotionally aligned and comforting.

Reduced robotic tone; more natural and conversational.

Model occasionally over-emphasizes empathy; future tuning may balance it.

8. Limitations

Empathy may drop when conversations become very long.

Model sometimes mirrors user emotions too strongly (e.g., repeating user's negative tone).

High-quality Bengali datasets are still limited compared to English.

9. Future Scope

Add voice-based Bengali empathetic model using Whisper + TTS.

Introduce persona-based empathy (doctor, teacher, counselor, friend).

Expand dataset to include real Bengali counseling transcripts (with privacy protection).

Deploy as chatbot API with smart memory and conversation history.

10. Real-World Applications

Mental health support assistants

Customer service agents

Educational chatbots

Eldercare communication bots

Bengali-friendly AI assistants for rural areas

