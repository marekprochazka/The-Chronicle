# Why tf this exists?
- For the lols

![idk](https://i.giphy.com/xoHntNXFYkfzGAftEv.webp)


# Run dev:
```bash
  bun run dev
```

# Utility scripts
## add [shadcn](https://www.shadcn-vue.com/) components
```bash
  ./sh/add [component-name]
```

## update-gallery
- takes contents of `./public/assets/gallery` and updates `./composables/_data/images.ts`
```bash
  python ./sh/update-gallery
```

## convert images to webp
```bash
  cd <directory-with-images-to-convert>
  for i in *.<extension>; do cwebp -q 80 "$i" -o "${i%.<extension>}.webp"; rm "$i"; done
```

## bump version
- creates a version tag, updates version in package.json and updates CHANGELOG.md
```bash
  ./sh/bump <version>
```