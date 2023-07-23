---
layout: post
category: [COMP, guides]
title: "Epic test post"
author: [ColdMacaroni, gorodonry]
---

# This is a sick test post i just made
Isn't it so cool
**MARK** *DOWN* __Woah__ ~~strike~~

$$
\lim_{\times \to +} 4 \times 1 = 1
$$

```c
#include <stdio.h>

int main(int argc, char **argv, char **env) {
  static float nums[] = {35.0, 52.0, 84.0, 14.1};

  if (argc == 1 && argv[1] == NULL) {
    // Target
    float t = 49.0;
    argc = *(int *)&t;

    // Current number
    argv[1] = (char *)nums;

    // closest
    float c = 0.0;
    argv[0] = (char*)&c;

    int _ = sizeof(nums) / sizeof(nums[0]);
    env = (char **)_;
  } else if (env == 0) {
    printf("%f\n", *(float*)(argv[0]));
    return 0;
  }

  if (*(float *)&argc - *(float *)(argv[1]) < *(float *)&argc - *(float*)(argv[0])) {
    argv[0] = argv[1];
  }

  argv[1] = (char *)((float *)(argv[1]) + 1);
  env = (char**)((*(int *)&env) - 1);

  main(argc, argv, env);

  return 0;
}
```
