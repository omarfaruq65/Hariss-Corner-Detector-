# Hariss-Corner-Detector-
## Hariss Corner Detector own function 
<b>Harris Corner Detector Algorithm</b> <br>
<ol>
    <li>Compute X and Y derivatives of image</li>
    \begin{equation}
        I_x = G_{\sigma}^x * I \quad \quad \quad
        I_y = G_{\sigma}^y * I
    \end{equation}
    <li>Compute products of derivatives at every pixel</li>
    \begin{equation}
        I_{x^2} = I_x . I_x \quad \quad \quad
        I_{y^2} = I_y . I_y \quad \quad \quad
        I_{xy} = I_x . I_y 
    \end{equation}
    <li>Compute sum of the products of derivatives at every pixel</li>
    \begin{equation}
        S_{x^2} = G_{\sigma^{\prime}} * I_{x^2} \quad \quad \quad
        S_{y^2} = G_{\sigma^{\prime}} * I_{y^2} \quad \quad \quad
        S_{xy} = G_{\sigma^{\prime}} * I_{xy}
    \end{equation}
    <li>Define the Matrix at every pixel</li>
        \[
            M(x,y)=
                \begin{bmatrix}
                S_{x^2}(x,y) & S_{xy}(x,y) \\
                S_{xy}(x,y) & S_{y^2}(x,y) 
                \end{bmatrix}
        \]
    <li>Compute the response of the detector at each pixel</li>
    \begin{equation}
        R = det(M) - k(trace M)^2
    \end{equation}
    <li>Threshold on value of R; compute non-max suppression.</li>
</ol>
