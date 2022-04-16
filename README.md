## About The Project

- Build Responsive Real-World Websites with HTML and CSS
- Learn modern HTML5, CSS3 and web design by building a stunning website for your portfolio! Includes flexbox and CSS Grid
- Tutorial for CSS Layouts
- [GitHub - Jonas Schmedtmann](https://github.com/jonasschmedtmann)
- [GitHub - Original Repo](https://github.com/jonasschmedtmann/html-css-course)

&nbsp;

## Notes

- [MDN - Mastering margin collapsing](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing)
- [Malven Co. - Flexbox cheatsheet](https://flexbox.malven.co/)
- [FLEXBOX FROGGY](https://flexboxfroggy.com/)
- [mastery.games](https://mastery.games/)

### Challenges

- [Section 3 - Challenge 3 - Position](https://codepen.io/jonasschmedtmann/pen/dyNwwGP/7a64f0845fd4f6439b63203371edbcb1)
- [Section 4 - Challenge 1 - Floats](https://codepen.io/jonasschmedtmann/pen/eYgbXrV/1a12771af64312342aa5a5f45bd2347c)
- [Section 4 - Challenge 2 - Flexbox](https://codepen.io/jonasschmedtmann/pen/MWJZZQL/c8e97f50f726b8e57ff58068647cde00)

&nbsp;

---

&nbsp;

> <b>Kulaj: </b><code>flex-grow:1</code> and <code>flex:1</code> are not the same result. Isn't it?
>
> First of all I want to say thank you very much for helping those who are in trouble like me. You mentioned that the <code>flex-grow:1</code> and <code>flex:1</code> gives us the same result. At 09:34 when you changes <code>flex-grow:1</code> to <code>flex:1</code> you said that we got the same result. But if you watch carefully you can see it is not the same result.
>
> When <code>flex-grow:1</code> all divs hadn't the same width, because you mentioned <code>flex-grow:1</code> means all divs get the remaining space evenly not get the same width. Yes I agree to that. When you changed <code>flex-grow:1</code> to <code>flex:1</code> you said result will be the same.
>
> But it wasn't the same. After you refreshed the browser, all the divs got the same width not the space evenly. I guess you haven't seen it because it is a small difference. I even put a ruler on my screen and measured it (I know it is silly😁).
>
> I really don't know what happened when you changed <code>flex-grow:1</code> to <code>flex:1</code> because I new to css. If it hasn't really changed then explain it to me. I'm sorry if this is a ridiculous question.

> <b>Jonas: </b>That's a very good observation, and you are absolutely right that these two results are a bit different 😃
>
> So, actually, <code>flex-grow: 1</code> and flex: 1 are not the exact same thing. Remember how the default for <code>flex-basis</code> (basically the width of flex items) is set to auto. So, when we set <code>flex-grow: 1</code>, the value for <code>flex-basis</code> will of course remain unchanged.
>
> However, flex: 1 will not only set <code>flex-grow: 1</code>, but it will also change <code>flex-basis</code> to 0. So, basically, the difference between flex: 1 and <code>flex-grow: 1</code> is that the first sets <code>flex-basis: 0</code>, while the second will keep the default of <code>flex-basis: auto</code>. I know this looks a bit confusing, so read it multiple times :) I hope this makes sense!

> <b>Tanish: </b>Thank you so much for posting this question, else i'd never know that <code>flex:1</code> and <code>flex-grow:1</code> are indeed different.
>
> I also did the math and came up with the following : -
>
> <code>flex:1</code> Here, each flex item will flex to the exact same size. So, get the container's width and divide it equally among all the flex items. Since flex-basis is set to 0 because of using short-hand property, this makes sense. Browser has taken the responsibility of assigning equal part of the container's width to each of the flex item.
>
> <code>flex-grow:1</code> As the name suggests, this will grow each flex item by equal unit. So, all the flex items will not end up having the same width, but will be increased by same unit. (That same unit can be calculated by dividing the original extra space by the no. of flex items). Since, flex-basis is set to auto by default, it makes sense here, intuitively.

&nbsp;

---

&nbsp;

> <b>Krish: </b>Difference Between width & flex-basis

> <b>Boobalan: </b>flex basis is entirely different from width. flex basis work based on flex-direction. If flex direction is row then flex basis act as a width, if flex direction is column then flex basis act as a height. If you use both width or height and flex basis it will override width or height other than flex-basis value is set to auto.
>
> You can only use flex basis for flex items. but, you can use width property to all. flex basis is act based on main axis and it has a short hand property like flex:flex-grow flex-shrink flex-basis; (i.e., 1 0 450px;) If you use width you need to again mention flex grow flex shrink which will increase your line of code.
>
> If you use flex-basis: auto; then it will check for width or height value based on main axis. If width or height is not set then it will automatically take content width or height. hope it would clarify your question. thank you for this question

> <b>Jonas: </b>Just want to add to Boobalan's answer that using <code>width</code> on a flex items will sometimes interfere with size calculations of other elements. I have had problems with it in the past, and so I advise to never use <code>width</code> on flex items.
