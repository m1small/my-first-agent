# Landing Page Layout

## Component Order
1. headline.md
2. bio.md
3. badges.md
4. cta-button.md

## HTML Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Matt Small - Principal Consultant specializing in FinOps, Enterprise AI adoption, and Cloud strategy. 15+ years driving transformation at Fortune 500 companies and startups.">
    <title>Matt Small - Principal Consultant</title>
    <style>/* Inline CSS */</style>
</head>
<body>
    <main role="main">
        <!-- Components here -->
    </main>
</body>
</html>
```

## CSS Reset
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

## Body
display: flex
flex-direction: column
justify-content: center
align-items: center
min-height: 100vh
padding: 20px
background-color: #313357
color: #C0C0C0
font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif
line-height: 1.6

## Main
max-width: 800px
width: 100%
text-align: center
padding: 40px 20px (desktop)
padding-mobile: 20px 15px (≤768px)
