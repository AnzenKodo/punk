<!-- Punk Pallet -->
<div align="center">

![Screenshort](https://raw.githubusercontent.com/AnzenKodo/assests/main/punk/mono/logo.png)

[![Try Out](https://img.shields.io/badge/try_out-0583f2.svg?labelColor=F20544&style=for-the-badge)](https://bulletproof.italic.space/lettering?preload=https%3A%2F%2Fraw.githubusercontent.com%2FAnzenKodo%2Fpunk-mono%2Fmaster%2Fpunk-mono%2Fttf%2Fpunk-mono-bold.ttf&preload=https%3A%2F%2Fraw.githubusercontent.com%2FAnzenKodo%2Fpunk-mono%2Fmaster%2Fpunk-mono%2Fttf%2Fpunk-mono-regular.ttf)

</div>

Punk Mono is a monospace font, it's a custom build of [Iosevka](http://be5invis.github.io/Iosevka)
font. It focuses on simplicity, readability, and style.

## Preview

### Letters, Numbers and Symbols
```bash
# Capital letters
ABCDEFGHIJKLMNOPQRSTUVWXYZ

# Letters
abcdefghijklmnopqrstuvwxyz

# Numbers
1234567890

# Symbols
!@#$%^&*()_+{}:"<>?-=[];',./~`
```
![Preview](https://raw.githubusercontent.com/AnzenKodo/assests/main/punk/mono/preview.png)

#### Ligatures
```bash
-<< -< -<- <-- <--- <<- <- -> ->> -> ---> ->- >- >>- =<< =< =<= <== <=== <<= <=
=> ==>> ==> ===> =>= >= >>= <-> <--> <---> <----> <=> <==> <===> <====> ----->
<~~ <~ ~> ~~> :: ::: == /= ~= <> == != =/= =!= := :- :+ <* <*> *> <| <|> |> <.
<.> .> +: -: =: :> __ (* *) [| |] {| |} ++ +++ \/ /\ |- -| <!- <!-- <***>
```
**Ligatures on**
![Ligatures on preview](https://raw.githubusercontent.com/AnzenKodo/assests/main/punk/mono/lint.png)

**Ligatures off**
![Ligatures off preview](https://raw.githubusercontent.com/AnzenKodo/assests/main/punk/mono/lint-off.png)

## Customized

To customize the font you can go to [Iosevka website](https://typeof.net/Iosevka/customizer).

## Building

### From the source

1. Install [`nodejs`](https://nodejs.org/en/download/) (≥ 14.0.0) and [`ttfautohint`](https://freetype.org/ttfautohint)
2. [Download](https://github.com/be5invis/Iosevka/archive/refs/heads/master.zip) the zip [Iosevka](https://github.com/be5invis/Iosevka) repository or Clone it:
	- (I recommend downloading the zip of repository instead of cloning it,
		because cloning will (1GB<=) to download where as downloading the zip will
		take (20MB<=)).
```bash
git clone https://github.com/be5invis/Iosevka.git
```
3. Move the [`private-build-plans.toml`](private-build-plans.toml) file to downloaded Iosevka repository.
4. Go to Iosevka repository.
5. Run `npm install`. This command will install all the NPM dependencies, and
	 will also validate whether external dependencies are present.
7. After finishing install dependencies, run
	 `npm run build -- contents::iosevka`. This will take hours depends on your
	 machine.
9. After finishing building you will find TTFs, as well as WOFF(2) web fonts and
	 one Webfont CSS in the dist/ directory.

### Using a Docker container

1. A Docker container handling the build environment for you can be found
	 [here](https://github.com/avivace/iosevka-docker).
2. Provide [`private-build.plans.toml`](private-build.plans.toml) for a
	 customized build and/or specify the desired release appending
	 `-e FONT_VERSION=X.X.X` to the Docker command.
4. To pull it from Docker Hub and start a standard build of the latest released
	 version, run
	 ```bash
	 docker run -it -v $(pwd):/build avivace/iosevka-build
	 ```
	 Or if you are using Powershell, run

   ```bash
   docker run -it -v ${pwd}:/build avivace/iosevka-build
   ```
