\documentclass[tikz, border=10pt]{standalone}
\usepackage[utf8]{inputenc}
\usepackage{tikz}
\usetikzlibrary{mindmap, trees, shadows}

% Color Definitions for clarity
\definecolor{rootcolor}{RGB}{40, 40, 40}      % Dark Grey
\definecolor{calculuscolor}{RGB}{200, 50, 50} % Red
\definecolor{derivcolor}{RGB}{50, 100, 200}   % Blue
\definecolor{prodcolor}{RGB}{50, 150, 50}     % Green
\definecolor{financecolor}{RGB}{200, 150, 0}  % Orange

\begin{document}

\pagestyle{empty}

\begin{tikzpicture}[
    mindmap,
    grow cyclic,
    every node/.style=concept,
    concept color=rootcolor,
    text=white,
    level 1/.style={level distance=5cm, sibling angle=90},
    level 2/.style={level distance=3cm, sibling angle=45},
    every annotation/.style={fill=white, text=black, align=left, drop shadow}
]

% --- Central Node ---
\node{Stochastic Calculus \\ \& Itô's Lemma}
    child [concept color=calculuscolor] {
        node {Itô Basics \\ \& The "Box"}
        child { node {Multiplication Table} 
            % Annotation for the critical rule
            node [annotation, left, xshift=-0.5cm] {
                \textbf{Golden Rule:} \\
                $dW \cdot dW = dt$ \\
                $dt \cdot dW = 0$ \\
                $dt \cdot dt = 0$
            }
        }
        child { node {Mechanical Routine} 
            node [annotation, below] {
                1. Compute $f_t, f_x, f_{xx}$ \\
                2. Substitute $dX$ \\
                3. Taylor Expand \& Box Rules
            }
        }
        child { node {Convexity Adj.} 
            node [annotation, right] {
                $\frac{1}{2}\sigma^2 S^2 f_{xx}$ \\
                Why we add this term? \\
                Because $dW \sim \sqrt{dt}$ \\
                is too jagged!
            }
        }
    }
    child [concept color=derivcolor] {
        node {Key Derivations \\ (Diff. Shapes)}
        child { node {$\ln S$ \\ (Concave)} 
            node [annotation, left] {
                $f_{xx} < 0$ (Concave) \\
                Drift: $\mu - \frac{1}{2}\sigma^2$ \\
                \textit{Subtracts value}
            }
        }
        child { node {$1/S$ \\ (Convex)} 
            node [annotation, right] {
                $f_{xx} > 0$ (Convex) \\
                Drift: $\sigma^2 - \mu$ \\
                \textit{Adds value}
            }
        }
        child { node {Why different?} 
            node [annotation, below] {
                Isolating Drift depends on \\
                the \textbf{Second Derivative} sign.
            }
        }
    }
    child [concept color=prodcolor] {
        node {Product Rule \\ (The "Algorithm")}
        child { node {The Skeleton \\ (Fixed)} 
            node [annotation, left] {
                Always: \\
                $d(XY) = XdY + YdX + \mathbf{dXdY}$
            }
        }
        child { node {The "Cross Term" \\ (Variable)} 
            node [annotation, right, text width=4cm] {
                $\mathbf{dX \cdot dY}$ depends on source: \\
                1. Same $dW$: $\sigma^2 dt$ \\
                2. Indep $dW$: $0$ \\
                3. Deterministic: $0$
            }
        }
    }
    child [concept color=financecolor] {
        node {Financial \\ Meaning}
        child { node {Isolating Drift} 
            node [annotation, left] {
                Grouping all $dt$ terms. \\
                If Drift $= 0 \to$ Martingale.
            }
        }
        child { node {Origin of $\mu$ \& $r$} 
            node [annotation, right] {
                Not from calculus! \\
                From Model Assumptions: \\
                $dS = \mu S dt + \dots$ \\
                $dB = r B dt$
            }
        }
        child { node {Example: $d(S/B)$} 
             node [annotation, below] {
                Combines Product Rule \\
                with Model Assumptions.
             }
        }
    };

\end{tikzpicture}

\end{document}
