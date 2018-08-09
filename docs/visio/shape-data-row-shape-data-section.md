---
title: Linha Shape Data (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251344
localization_priority: Normal
ms.assetid: f3a83496-fccc-9d6a-02b9-60ebaf4911ea
description: Contém a informação para um único item de dados da forma associado a uma forma. Uma forma contém uma linha Shape Data para cada propriedade personalizada.As linhas Shape Data são denominadas Prop.name e contêm as células a seguir. Para obter mais detalhes, consulte os tópicos específicos das células.
ms.openlocfilehash: 7bf7eafd1869aa3c3ee03efbde30560cdaaeb302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772867"
---
# <a name="shape-data-row-shape-data-section"></a>Linha Shape Data (Seção Shape Data)

Contém a informação para um único item de dados da forma associado a uma forma. Uma forma contém uma linha Shape Data para cada propriedade personalizada.As linhas Shape Data são denominadas Prop.name e contêm as células a seguir. Para obter mais detalhes, consulte os tópicos específicos das células.
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[Label](label-cell-shape-data-section.md) <br/> |Especifica o rótulo exibido aos usuários na janela ou na caixa de diálogo **Shape Data**.  <br/> |
|[Prompt](prompt-cell-shape-data-section.md) <br/> |Especifica o texto descritivo ou instrucional exibido aos usuários na janela ou na caixa de diálogo **Shape Data** quando o item é selecionado.  <br/> |
|[Tipo](type-cell-shape-data-section.md) <br/> |Especifica um tipo de dado para o valor do item de dados da forma: sequência de caracteres (0), lista fixa (1), número (2), valor booleano (3), lista variável (4), data ou hora (5), duração (6) ou moeda (7).  <br/> |
|[Format](format-cell-shape-data-section.md) <br/> |Especifica a formatação de um item de dados da forma.  <br/> |
|[Valor](value-cell-shape-data-section.md) <br/> |Contém o valor do item inserido na janela ou na caixa de diálogo **Shape Data**.  <br/> |
|[SortKey](sortkey-cell-shape-data-section.md) <br/> |Especifica uma chave pela qual os itens na janela ou na caixa de diálogo **Shape Data** são listados.  <br/> |
|[Invisível](invisible-cell-shape-data-section.md) <br/> |Especifica se o item de dados da forma será visível na janela ou na caixa de diálogo **Shape Data**. VERDADEIRO = invisível; FALSO = visível.<br/> |
|[Peça](ask-cell-shape-data-section.md) <br/> |Determina se um usuário é solicitado a inserir as informações de dados de forma para uma forma quando uma instância é criada ou a forma é duplicada ou copiada.  <br/> |
|[LangID](langid-cell-shape-data-section.md) <br/> |Especifica o idioma em que será exibido o valor do item de dados da forma.  <br/> |
|[Calendário](calendar-cell-miscellaneous-section.md) <br/> |Especifica o tipo de calendário a ser usado quando o Tipo de um item de dados for Data.  <br/> |
   
## <a name="remarks"></a>Comentários

 Você pode adicionar tantos Prop.  linhas de *nome* conforme necessário, atribuir nomes significativos às linhas e definir valores de célula. Para adicionar um item de dados de forma a uma seção de dados da forma existente, do mouse em uma linha e clique em **Inserir linha** no menu de atalho. 
  
Você pode fazer referência a essas células pelo nome da linha, exibido em uma janela ShapeSheet em texto vermelho. Para atribuir nomes significativos às linhas Prop. linhas de *nome* , clique na linha e digite um nome como *preço* , por exemplo, para criar o nome da linha Prop. Você pode fazer referência à célula Label usando Prop.Price.Label. 
  
O nome de linha inserido deve ser único na seção.
  

