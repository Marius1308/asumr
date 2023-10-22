``` {.tex .render height=540px}
\documentclass{standalone}
\usepackage{tikz}

\begin{document}
\begin{tikzpicture}
  % Draw x-axis with stealth arrowhead
  \draw[-stealth, red!90!black, line width=1pt] (0,0) -- (4,0) node[right] {$X_I$};
  % Draw y-axis with stealth arrowhead
  \draw[-stealth,green!60!black, line width=1pt] (0,0) -- (0,4) node[above] {$Y_I$};
  % Draw car body at position (3,3) and rotate by 30 degrees
  \draw[fill=blue!50!white,rotate=30] (2,0.) rectangle ++(1,0.5);
  % Draw wheels
  \draw[fill=black,rotate=30] (2.6,-0.1) rectangle ++(0.3,0.1);
  \draw[fill=black,rotate=30] (2.6,0.5) rectangle ++(0.3,0.1);
  \draw[fill=black,rotate=30] (2.1,-0.1) rectangle ++(0.3,0.1);
  \draw[fill=black,rotate=30] (2.1,0.5) rectangle ++(0.3,0.1);
  % Draw local coordinate system "x_car" and "y_car" with stealth arrowheads
  \draw[-stealth, red!90!black, rotate=30, line width=1pt] (2.5,0.25) -- ++(1.,0) node[above right] {$X_{car}$};
  \draw[-stealth, green!60!black, rotate=30, line width=1pt] (2.5,0.25) -- ++(0,1) node[above left] {$Y_{car}$};
  \draw[dashed,-] (2.04, 0) -- (2.04,1.48) node[below left] {$P$};
  \draw[dashed,-] (0, 1.48) -- (3.,1.48) node[above] {$\theta$};
  \draw[stealth-] (2.6, 1.77) arc (30:0:0.6);

\end{tikzpicture}
\end{document}
```