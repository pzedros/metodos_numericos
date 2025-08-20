# Relatório de Tarefas de Métodos Numéricos

## 📑 Sumário
- [1. Análise de Erros](#1-análise-de-erros)
- [2. Cálculo de Raízes de Equações Não Lineares](#2-cálculo-de-raízes-de-equações-não-lineares)
- [3. Otimização Unidimensional](#3-otimização-unidimensional)
- [4. Sistemas Lineares e Não Lineares](#4-sistemas-lineares-e-não-lineares)
- [5. Ajuste de Curvas](#5-ajuste-de-curvas)
- [6. Integração e Derivação Numérica](#6-integração-e-derivação-numérica)

---

## 1. Análise de Erros
Este trabalho avalia a precisão e a convergência de séries numéricas aplicadas ao cálculo do cosseno via série de Maclaurin e à soma de uma p-série.  

**Série de Maclaurin para o cosseno:**  
As aproximações foram feitas em Python, analisando os erros percentuais estimados e verdadeiros. Os testes revelaram que os métodos numéricos implementados são eficazes e proporcionam alta precisão, com erros tendendo rapidamente a zero à medida que as iterações aumentam.  

---

## 2. Cálculo de Raízes de Equações Não Lineares
Foram aplicados os métodos de Bisseção, Falsa Posição, Newton-Raphson, Secante e Secante Modificada para determinar raízes de funções.  
Os algoritmos foram avaliados quanto à velocidade de convergência, precisão e robustez.  
- **Newton-Raphson**: mais eficiente quando iniciado com boas estimativas.  
- **Bisseção e Falsa Posição**: maior estabilidade, mas menor velocidade.  

---

## 3. Otimização Unidimensional
O problema de otimização abordou o projeto de um recipiente cilíndrico aberto com volume fixo, buscando o menor custo possível.  

- Resolução analítica: derivada.  
- Resolução numérica: Razão Áurea e Interpolação Quadrática.  
- **Resultado**: todos os métodos convergiram para o mesmo mínimo global.  
  - Raio = 5 cm  
  - Altura = 15 cm  
  - Custo total mínimo = **R$ 35,34**  

---

## 4. Sistemas Lineares e Não Lineares
Aplicação de métodos diretos e iterativos em problemas reais de engenharia.  

- **Lineares**: Eliminação de Gauss com Pivotamento, Jacobi, Gauss-Seidel e Gauss-Seidel com Relaxamento.  
- **Não lineares**: Newton-Raphson e método gráfico.  

**Destaque:** escolha adequada do método é essencial. Pivotamento pode viabilizar métodos iterativos em sistemas inicialmente instáveis.  

---

## 5. Ajuste de Curvas
Objetivo: encontrar uma função matemática que melhor represente um conjunto de dados discretos.  

### Regressão por Mínimos Quadrados
- Linear Simples: `y = a0 + a1x`  
- Polinomial: polinômios de grau superior  
- Múltipla: mais de uma variável independente  
- Não Linear: modelos como exponencial, potência e crescimento  
- Qualidade do ajuste: **R² (coeficiente de correlação)**  

### Interpolação
- Polinomial: polinômio de grau `n-1` que passa por `n` pontos  
- Newton (diferenças divididas): útil quando o grau é desconhecido  
- Lagrange: prático quando o grau já é definido  

**Aplicações:** prever valores intermediários, ajustar dados experimentais e avaliar modelos em engenharia.  

---

## 6. Integração e Derivação Numérica

### Integração Numérica
Usada quando a integral exata é difícil ou impossível de calcular.  

- **Newton-Cotes:**  
  - Regra do Trapézio  
  - Trapézio Múltiplo  
  - Regra 1/3 de Simpson  
  - Regra 3/8 de Simpson  
  - Quadratura de Gauss  

### Derivação Numérica
Aplicada quando a função é conhecida apenas em pontos discretos.  

- Baseada na série de Taylor.  
  - Primeira Derivada:  
    - Progressiva: `f'(x) ≈ (f(x+h) - f(x)) / h`  
    - Regressiva: `f'(x) ≈ (f(x) - f(x-h)) / h`  
    - Centrada: `f'(x) ≈ (f(x+h) - f(x-h)) / (2h)` (mais precisa)  
  - Segunda Derivada: combina valores vizinhos.  
  - Alta Acurácia: fórmulas com mais termos da série de Taylor.  
  - Dados Desigualmente Espaçados: também possíveis de tratar.  

**Aplicações:** cálculo de áreas, médias de dados experimentais, fluxo de calor e estimativa de taxas de variação em fenômenos físicos.  

---
