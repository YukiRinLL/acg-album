# ACG-Album usage

[![license](https://img.shields.io/github/license/george-chou/acg-album.svg)](https://github.com/george-chou/acg-album/blob/master/LICENSE)

## Important links
|   Name    | URL                                        |
| :-------: | :----------------------------------------- |
|    Git    | <https://git-scm.com/downloads>            |
|  GitHub   | <https://github.com>                      |
| acg-album | <https://github.com/george-chou/acg-album> |
|  Vercel   | <https://vercel.com>                      |

## Git

Install Git: <a href="https://git-scm.com/downloads" target="_blank">git-scm.com/downloads</a>

## Custom

1. Register a GitHub account and fork a copy of this repository to your own account

2. Switch to the htdocs directory of XAMPP in cmd and clone the repository:
```
git clone https://github.com/%Your_GitHub_Account%/acg-album.git
```

3. In the `./acg-album` directory, you can see that there are two configuration files with the same structure, `config-37.json` and `config-rem.json` corresponding to `Theme March 7` and `Theme Rem` respectively, here is an example of `config-37.json`:

```
{
    "idol": "Name of your idol",
    "date": "Following time, the format is yyyy/mm/dd",
    "bgm": "BGM name",
    "bgmurl": "BGM source URL",
    "bgmsrc": "BGM audio direct link (it is best to get mp3 without API, it may be blocked by cross-domain)",
    "wallpaper": "wallpaper URL",
    "content": "Idol Classic Quotes",
    "pics": [
        "Album picture 1 href",
        "Album picture 2 href",
        ...
        "Album picture 15 href"
    ]
}
```

It can be customized as described above.

## Switch themes
Open `load.js` in the `./acg-album/js` directory and modify the first line of code:
```
let cfg = "./config-37.json";
```
Currently is `Theme March 7`, if you want to switch to `Theme Rem`, change it to:
```
let cfg = "./config-rem.json";
```

## Deploy to Vercel

Similar video tutorials are available at <https://www.bilibili.com/video/BV1wp4y1W7aH?p=2>

1. Sync the modified local code to your GitHub account:
```
cd acg-album
git add .
git commit -a
# i
# input commit description
# :wq!
git push
```

2. Enter <a href="https://vercel.com/login" target="_blank">Vercel official website</a>

3. Log in with your own GitHub account authorization, click `+ New Project`

4. Type the keyword acg-album in the search box of `Import Git Repository` to find the repository that was previously forked

5. Click `Import` to modify the `PROJECT NAME` under `Configure Project`

6. Make sure that `PROJECT NAME` does not conflict with others and click `Deploy`

7. After the deployment is complete, you can visit `https://%PROJECT_NAME%.vercel.app` in the WAN to view the webpage. (where `%PROJECT_NAME%` is the `PROJECT NAME` just modified under `Configure Project`)

## Future work

The style of this album has not been debugged on mobile clients, so it does not display properly on the mobile terminal. This problem will be fixed in the future.