# The Art of Readable Code

## Chapter 1. Code Should Be Easy to Understand

**_Code should be easy to understand._**

Over the past five years, we have collected hundreds of examples of “bad code” (much of it our own) and analyzed what made it worse, and what principles/techniques were used to make it better. What we noticed is that all of the principles stem from a single theme.

>*Trong năm năm qua, chúng tôi đã thu thập hàng trăm ví dụ về mã xấu Bad (phần lớn là của chúng tôi) và phân tích điều gì làm cho nó tồi tệ hơn, và những nguyên tắc / kỹ thuật nào được sử dụng để làm cho nó tốt hơn. Những gì chúng tôi nhận thấy là tất cả các nguyên tắc bắt nguồn từ một chủ đề duy nhất.*

We believe this is the most important guiding principle you can use when deciding how to write your code. Throughout the book, we’ll show how to apply this principle to different aspects of your day-to-day coding. But before we begin, we’ll elaborate on this principle and justify why it’s so important.

>*Chúng tôi tin rằng đây là nguyên tắc hướng dẫn quan trọng nhất bạn có thể sử dụng khi quyết định cách viết mã của mình. Xuyên suốt cuốn sách, chúng tôi sẽ chỉ ra cách áp dụng nguyên tắc này cho các khía cạnh khác nhau của mã hóa hàng ngày của bạn. Nhưng trước khi bắt đầu, chúng tôi sẽ giải thích về nguyên tắc này và giải thích lý do tại sao nó lại rất quan trọng.*

What Makes Code “Better”?
Most programmers (including the authors) make programming decisions based on gut feel and intuition. We all know that code like this:
>*Hầu hết các lập trình viên (bao gồm cả các tác giả) đưa ra quyết định lập trình dựa trên cảm giác và trực giác. Chúng ta đều biết mã như thế này:*
```
for (Node* node = list->head; node != NULL; node = node->next)
    Print(node->data);
```
is better than code like this:
>*tốt hơn mã như thế này:*
```
Node* node = list->head;
if (node == NULL) return;

while (node->next != NULL) {
    Print(node->data);
    node = node->next;
}
if (node != NULL) Print(node->data);
```
