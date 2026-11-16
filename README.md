# A Transformer in Excel

**Type `three plus four equals` in Excel and follow a tiny transformer as it predicts the next token, `seven`.** The workbook shows the intermediate matrices in color-coded cells so you can trace how the prediction changes when you edit the prompt.

[**Download the Excel workbook (.xlsx)**](https://github.com/varbell/simple-excel-transformer/raw/refs/heads/main/simple_transformer_emulator.xlsx) · [View the workbook on GitHub](simple_transformer_emulator.xlsx)

<img width="1108" alt="The Excel workbook showing the addition prompt and color-coded transformer calculations" src="https://github.com/user-attachments/assets/2339513c-05dc-4bf1-be43-4f0f79e6eabc" />

## Try it in a minute

1. Download the workbook and open it in desktop Microsoft Excel. If Excel opens it in Protected View, enable editing to change the input.
2. Replace the example prompt with `three plus four equals` and press Enter. Look for `seven` in the output.
3. Change just one word, for example `three plus five equals`, and follow the changes from the input embeddings through attention to the next-token output.

Use spelled-out numbers from `one` to `nine` and start with sums below ten. The vocabulary has no token for zero and includes `ten`.

**See the matrices update side by side.** In Excel, choose **View → New Window** to open a second view of the same workbook. Keep the input visible in one window and scroll to the attention calculations in the other.

<img width="672" alt="The New Window command in Excel's View tab" src="https://github.com/user-attachments/assets/1577e393-3dd3-4287-b271-fb184c4871aa" />

## What to look for

| Stage | What to inspect |
| --- | --- |
| Token embeddings | Each of the four input words is represented by an eight-dimensional vector. Change one word and see which input row changes. |
| Rotary position embeddings (RoPE) | RoPE rotates queries and keys by position before attention scores are computed. |
| Multi-head attention | Compare the attention weights across the four heads after changing one operand. |
| Next-token output | See how the model scores the possible next tokens after `equals`. |

## Model at a glance

| Setting | Value |
| --- | --- |
| Task | Predict the next token after a four-word addition prompt |
| Transformer layers | 1 |
| Model dimension | 8 |
| Attention heads | 4 |
| Vocabulary | 12 tokens, `one` through `ten` plus `plus` and `equals` |
| Position encoding | RoPE |

The model was trained in Python, and its learned weights were copied into Excel. You can run the forward pass using the workbook alone.

If you use the workbook in a class or find a prompt that produces a surprising result, [open an issue](https://github.com/varbell/simple-excel-transformer/issues/new) with the four-word prompt and what Excel showed.

[MIT License](LICENSE)
