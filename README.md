# MusicTextAlignment
## Describe
This is a dataset that aligns **piano music MIDI** with their corresponding **textual descriptions and comments**. It can be used for multi-modal models in music-text alignment tasks, similar to how visual-LLM (such as LLaVA, MiniGPT4 and VisualGLM) align image encodings with textual embeddings. 

## Dataset collection method
1. The **piano music MIDI** files are sourced from an open dataset [*GiantMIDI-Piano*](https://github.com/bytedance/GiantMIDI-Piano) provided by ByteDance. 
2. The associated descriptions and comment **texts** are collected from the video descriptions and the top 5 comments in the comment section of the source YouTube videos for the music.

## Dataset Format
1. The data format for this project is TSV (Tab-Separated Values) files, where tab characters are used as separators to record information about music MIDI and its corresponding textual data.
2. The dataset examples:  

| index | old_id | vid         | describe                                                                                    | reply_1                                                                     | reply_2                                                                          | reply_3                                                                   | reply_4                                                                           | reply_5                                                                           |  
|-------|--------|-------------|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|  
| 0     | 1      | V8WvKK-1b2c | P.7 First Lesson 0:00. P.7 Up and Down 0:20. ... | "I played all these when I was learning to play as a kid in the 80s. Love this piano book! When I was about 7 years old, I started playing 'Evening Song' in a minor key because I thought it sounded better." | Wonderful and practical. I'm learning playing piano by this video. Appreciated for the useful lessons. | Спасибо большое за наглядное пособие по учебнику ️️️ | Thanks, very useful video, it’s really help for first timer. | I'm currently on the singing brook and the sharps and flats still intimidate and confuse me. But your videos are really helpful! Thank you! | 
|...|...|...|...|...|...|...|...|...|   

3. The dataset consists of 9 fields, namely: `index`, `old_id`, `vid`, `describe`, `reply_1`, `reply_2`, `reply_3`, `reply_4`, and `reply_5`. Here, `index` serves as the index number for each sample, `old_id` represents the preprocessed identifier (this field can be ignored by users), `vid` corresponds to the YouTube video ID (consistent with the 'vid' field in the [*GiantMIDI-Piano*](https://github.com/bytedance/GiantMIDI-Piano) dataset), `describe` is the text string of the video description set by the video uploader, and `reply_1` to `reply_5` are text strings of the top five comments in the comment section.
4. For information about the piano music MIDI audio file dataset, please refer to [*GiantMIDI-Piano*: https://github.com/bytedance/GiantMIDI-Piano](https://github.com/bytedance/GiantMIDI-Piano)

## Tips 
1. The textual data is collected from the Internet, hence there are significant differences in language, expression, and format. Please exercise discretion in assessing the data quality.
2. Please use the dataset within the specified guidelines. Any consequences arising from the use of the dataset are at your own risk.
