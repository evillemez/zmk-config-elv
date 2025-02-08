# Iteration with Claude

I used Claude at various stages to write, debug, and test the firmware.  I kept notes here for specific things I produced to give Claude extra info on issues I was having.

## Wiring 

This was created for helping Claude understand the wiring, so it could help me write the correct overlay and keymap files.

```
nice!nano pin -> keyboard function
P0.31 -> Column 0 (outer columns)
P0.29 -> Column 1 (pinky columns)
P0.02 -> Column 2 (ring columns)
P1.15 -> Column 3 (middle columns)
P0.20 -> Column 4 (index columns)
P0.22 -> Column 5 (inner columns)
...

P1.13 -> Row 0 (left top)
P1.11 -> Row 1 (left middle)
P0.10 -> Row 2 (left bottom)
P0.09 -> Row 3 (left thumb row)
...

P0.24 -> Row 4 (right top)
P1.00 -> Row 5 (right middle)
P0.11 -> Row 6 (right bottom)
P1.04 -> Row 7 (right thumb row)

...

Display connections:
SCL -> P0.08
SDA -> P0.06
CS -> P0.17
```

## Testing matrix

```
ESC [✓] Q[✗] W[✗] E[✓] R[✓] T[✓]
TAB [✗] A[✓] S[✓] D[✓] F[✗] G[✗]
SHIFT[✓] Z[✓] X[✓] C[✗] V[✓] B[✓]
CTRL[✓] GUI[✓] ALT[✓] L1[✓] L2[✓] SPACE[✓]

Y[✓] U[✓] I[✓] O[✗] P[✓] BSPC[✓]
H[✓] J[✓] K[✓] L[✓] ;[✓] '[✓]
N[✗] M[✓] ,[✓] .[✓] /[✓] SHIFT[✓]
RET[✓] L3[✗] ←[✓] ↓[✓] ↑[✓] →[✓]
```
