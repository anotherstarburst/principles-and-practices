---
layout: page
title: CSS unit conventions
---

## Choosing appropriate CSS units

Ideally we want all our CSS units to be relative to an abstract *base font size* value to that all the other styling will reflect changes to the base unit value.

Below is a suggested set of relative unit types however it is also okay to use calculations on an explicit font base size variable as long as it is performant.

## Padding and Margin

These should normally use `rem` units. Don't use more than two decimal places for these definitions.

## Relative sizing of elements of a container

These can be defined using percentage values which relate to the relative size of the parent container.

## Viewport/Page dimensions

When things should be sized relative to the viewport of the browser (which may often be phrased as in relation to the page size, a hangover from print design) you can use the viewport units `vh` and `vw`.

## Font sizes

The base font size can be sized in `px` but then all other font-sizes should be relative either using CSS variables and calculations, `rem` units or percentages of the base font.

## Borders

Thickness and radius are best expressed in `px` if they invariant.

Use `rem` if they are meant to be vary in thickness relative to accompanying content.

## Flexbox

Ideally the unitless measures should be used to describe flexbox relations ideally with percentages for width, height or spacing.