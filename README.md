# research
A repository where I store information I know and explain using photographs.

# Bresenham's line algorithm (short version)
```
  void dda(int x0, int y0, int x1, int y1) {
  int dx = abs(x1-x0);
  int dy = abs(y1-y0);
  int sx = x1 < x0 ? 1 : -1;
  int sy = y1 < y0 ? 1 : -1;
  int err = dx - dy;
  while(1) {
    if (x0>=0 && x0<HW && y0>=0 && y0<HW) buf[y0][x0]='1';
    if (x0==x1 && y0==y1) return;
    int e2 = err*2;
    if (e2 > -dy) { err-=dy; x0+=sx; }
    if (e2 < dx ) { err+=dx; y0+=sy; }
  }
}
```

This algorithm draws a line without using complex mathematical calculations and employs only integers.
Here is a rough example in photos:
