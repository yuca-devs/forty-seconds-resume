# Forty Seconds Resume - yuca template

This is a [yuca](https://github.com/yuca-devs/yuca) template based on the [Forty
Seconds CV](https://github.com/PandaScience/FortySecondsCV) project.

> The default user image was taken from [here](https://thinksport.com.au/life-members/attachment/default-avatar-profile-icon-grey-photo-placeholder-illustrations-vectors/).

## Install

```bash
yuca template get https://github.com/yuca-devs/forty-seconds-resume.git
```

## Template configuration parameters

A minimal yuca recipe to use this template could be:

```yaml
template: forty-seconds-resume
user_data: en.yml  # change if needed!

# Compile using lualatex
post_cook:
  - lualatex -file-line-error -synctex=1 -interaction=nonstopmode -recorder template.tex
  - lualatex -file-line-error -synctex=1 -interaction=nonstopmode -recorder template.tex
  - rm *.fls
  - rm *.log

# Template generation config
gen_config:
  # Files you can override
  files:
    profile_picture: path/to/profile/picutre.jpg  # change!

  # Default template settings
  settings:
    main_color: '0E5484'
    side_color: 'E7E7E7'
    section_color: '1E6494'
    subsection_color: '1D1D1D'
```

> Check the [yuca project](https://github.com/yuca-devs/yuca) for more
information on how to write a yuca recipe.
