# Simulador de Figuras de Chladni

Simulador de cimática: placa quadrada de bordas livres, vibrada pelo centro, com areia que migra para as linhas nodais.

- Informe uma frequência e veja a figura formada pela areia.
- Envie uma música: o simulador mostra o espectrograma, a frequência dominante em cada instante e gera as figuras correspondentes.

Tudo roda no navegador, num único arquivo `index.html`. O áudio enviado não sai do computador.

## Modelo

Equação de Kirchhoff para placas finas, `D∇⁴w + ρh ∂²w/∂t² = F·δ(x−x₀)·cos(2πft)`, com as quatro bordas livres. Os modos são calculados pelo método de Ritz (30×30 polinômios de Legendre) e a figura é a resposta forçada com amortecimento. A calibração padrão (aço, 0,755 mm, 24 cm) reproduz as fotos de referência do kit PASCO.

Validação com 21 fotos de três placas PASCO diferentes: a figura confere em 16 (76 %), e em 12 de 14 abaixo de 1100 Hz.
