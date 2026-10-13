**Respostas Etapa 2 AT 7**
1. **Árvores:** Foram usadas **80 árvores** (`n_estimators=80`).
2. **Threshold:** O valor é **0.60** (60%).
3. **Resultado:**
 [NLU] Modelo Random Forest e Vetorizador TF-IDF treinados com sucesso!

--- BATERIA DE TESTES DE ESTRESSE NLU ---

```
Entrada: 'Tenho 30 kg de banana para doar'
Intenção: cadastrar_doacao | Confiança: 0.93
Retorno: Intenção 'cadastrar_doacao' identificada com 92.5% de confiança.

Entrada: 'Nossa instituição precisa de mantimentos'
Intenção: fallback | Confiança: 0.41
Retorno: Desculpe, não consegui entender com clareza o seu pedido. 
Você pode refazer a mensagem informando se deseja **doar alimentos** ou **solicitar doações para uma ONG**?

Entrada: 'Qual é a receita de bolo de cenoura?'
Intenção: fallback | Confiança: 0.49
Retorno: Desculpe, não consegui entender com clareza o seu pedido. 
Você pode refazer a mensagem informando se deseja **doar alimentos** ou **solicitar doações para uma ONG**?

Entrada: 'coisa comida doar la'
Intenção: fallback | Confiança: 0.42
Retorno: Desculpe, não consegui entender com clareza o seu pedido. 
Você pode refazer a mensagem informando se deseja **doar alimentos** ou **solicitar doações para uma ONG**?
```

4. **Melhorias:** Adicionar mais dados no array de treino usando sinônimos, aplicar pré-processamento de texto (como *stemming*) e remoção de *stopwords*.

5. **Por que Random Forest:** Porque ele lida muito bem com matrizes esparsas geradas por vetorizadores TF-IDF, é extremamente leve para treinar localmente e usa *Bagging* para evitar o overfitting com poucos dados.
