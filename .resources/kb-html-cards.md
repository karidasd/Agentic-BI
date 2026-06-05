# Knowledge Base: Custom HTML KPI Cards in Power BI

This guide explains how to use AI to generate DAX code for custom KPI cards using the **HTML Viewer** custom visual in Power BI. This technique replaces native KPI cards with highly customizable HTML/CSS designs directly rendered via DAX.

## Overview
Power BI's native cards have limitations. By using an AppSource custom visual called **HTML Viewer**, we can write DAX measures that return a string containing HTML and inline CSS. The visual renders this string as a rich webpage, allowing for complex layouts, conditional formatting, icons, and micro-animations.

## DAX Pattern for HTML Cards

When tasked with creating an HTML KPI card, structure the DAX measure as follows:

1. **Variables for Metrics**: Define variables for the core metrics, targets, and formatted text.
2. **Conditional Logic**: Define variables for colors or icons based on conditions (e.g., Target met vs missed).
3. **HTML Construction**: Build the final HTML string, concatenating the variables inside an HTML container (like a `<div>`). Use inline CSS or `<style>` blocks for styling.

### Example DAX Code:

```dax
Sales KPI HTML Card = 
VAR CurrentSales = [Total Sales Amount]
VAR TargetSales = [Target Sales Amount]
VAR Variance = CurrentSales - TargetSales
VAR IsPositive = Variance > 0

VAR MetricColor = IF(IsPositive, "#28a745", "#dc3545")
VAR Arrow = IF(IsPositive, "▲", "▼")

VAR HtmlContent = 
"
<div style='font-family: Arial, sans-serif; padding: 20px; border-radius: 10px; background-color: #f8f9fa; box-shadow: 2px 2px 10px rgba(0,0,0,0.1); width: 250px;'>
    <div style='font-size: 14px; color: #6c757d; font-weight: bold;'>Total Sales</div>
    <div style='font-size: 32px; font-weight: bold; margin: 10px 0;'>$" & FORMAT(CurrentSales, "#,##0") & "</div>
    <div style='font-size: 16px; color: " & MetricColor & ";'>
        " & Arrow & " $" & FORMAT(ABS(Variance), "#,##0") & " vs Target
    </div>
</div>
"

RETURN HtmlContent
```

## Best Practices
- **Styling**: Use clean, modern CSS. Avoid generic colors; use HSL or modern palettes.
- **Responsiveness**: Use relative units (%, vw, vh) or flexbox where appropriate.
- **Performance**: Keep the HTML string concise. Avoid pulling in massive external libraries inside the measure.
- **Visual Assignment**: The resulting measure MUST be categorized as an Image URL or rendered using the "HTML Viewer" visual in Power BI.
