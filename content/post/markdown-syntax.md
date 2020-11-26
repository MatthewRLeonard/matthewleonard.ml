---
aliases:
- migrate-from-jekyl
author: Hugo Authors
categories:
- themes
- syntax
date: "2019-03-11"
description: Sample article showcasing basic Markdown syntax and formatting for HTML elements.
featured: true
series:
- Themes Guide
tags:
- markdown
- css
- html
- themes
- featured
thumbnail: images/building.png
title: Markdown Syntax Guide
---

This article offers a sample of basic Markdown syntax that can be used in Hugo content files, also it shows whether basic HTML elements are decorated with CSS in a Hugo theme.
<!--more-->

## Headings

The following HTML `<h1>`—`<h6>` elements represent six levels of section headings. `<h1>` is the highest section level while `<h6>` is the lowest.

# H1
## H2
### H3
#### H4
##### H5
###### H6

## Paragraph

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin re plis aut quas inctum laceat est volestemque commosa as cus endigna tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am facea corem alique molestrunt et eos evelece arcillit ut aut eos eos nus, sin conecerem erum fuga. Ri oditatquam, ad quibus unda veliamenimin cusam et facea ipsamus es exerum sitate dolores editium rerore eost, temped molorro ratiae volorro te reribus dolorer sperchicium faceata tiustia prat.

Itatur? Quiatae cullecum rem ent aut odis in re eossequodi nonsequ idebis ne sapicia is sinveli squiatum, core et que aut hariosam ex eat.

## Blockquotes

The blockquote element represents content that is quoted from another source, optionally with a citation which must be within a `footer` or `cite` element, and optionally with in-line changes such as annotations and abbreviations.

#### Blockquote without attribution

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **Note** that you can use *Markdown syntax* within a blockquote.

#### Blockquote with attribution

> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

## Tables

Tables aren't part of the core Markdown spec, but Hugo supports supports them out-of-the-box.

   Name | Age
--------|------
    Bob | 27
  Alice | 23

#### Inline Markdown within tables

| Italics   | Bold     | Code   |
| --------  | -------- | ------ |
| *italics* | **bold** | `code` |

## Code Blocks

#### Code block with backticks

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
<!-- this line is extraneous 2Error from server (Forbidden): deployments.apps is forbidden: User "chiptest" cannot create resource "deployments" in API group "apps" in the namespace "default" -->
</html>
```

#### Code block indented with four spaces

    <!doctype html>
    <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>Example HTML5 Document</title>
    </head>
    <body>
      <p>Test</p>
    </body>
    </html>

#### Code block with Hugo's internal highlight shortcode
{{< highlight html >}}
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
{{< /highlight >}}


### ticks then r

```r
games %>%
  filter(week %in% c("1", "2"), posteam %in% c("ARI", "SF")) %>%
  select(week, play_id, posteam, drive, score_differential_post, yardline_100, down, ydstogo, play_type, yards_gained, touchdown, ydsnet, drive_start_yard_line, drive_end_yard_line, drive_play_id_started, drive_off_play_id_started, drive_play_id_ended, drive_end_transition, ep, epa, wpa, away_wp_post, drive_play_count) %>%
  #filter(play_id == drive_off_play_id_started) %>%
  gt() %>%
    cols_label(
      play_id = "id",
      posteam = "ball",
```

See that!

### Using highlight then r

{{< highlight r >}}
# big join 
team_stats <- off_season_yards %>%
  full_join(def_season_yards, by = c("off_team" = "def_team")) %>%
  rename(team = "off_team") %>%
  full_join(off_team_stats) %>%
  full_join(def_team_stats) %>%
  left_join(select(teams, team_logo_wikipedia, team_abbr), by = c("team" = "team_abbr")) %>%
  left_join(select(standings, division, team)) %>%
  rename(logo = team_logo_wikipedia) %>%
  relocate(c("off_total_plays", "off_epa_pp", "off_success_rate", "off_explosiveness", "off_negatives", "def_total_plays", "def_epa_pp", "def_success_rate", "def_explosiveness", "def_negatives"), .after = "team") %>%
  relocate(c("logo", "division"), .after = "team")
{{< /highlight >}}

And that!


## List Types

#### Ordered List

1. First item
2. Second item
3. Third item

#### Unordered List

* List item
* Another item
* And another item

#### Nested list

* Fruit
  * Apple
  * Orange
  * Banana
* Dairy
  * Milk
  * Cheese

## Other Elements — abbr, sub, sup, kbd, mark

<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Press <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd></kbd> to end the session.

Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.
