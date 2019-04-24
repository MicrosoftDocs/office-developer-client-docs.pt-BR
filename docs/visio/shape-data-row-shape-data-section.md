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
description: Contém a informação para um único item de dados da forma associado a uma forma. Uma forma contém uma linha de dados da forma para cada item de dados da forma. As linhas de dados da forma são denominadas Prop.name e contêm as células a seguir. Para obter mais detalhes, consulte os tópicos específicos das células.
ms.openlocfilehash: 058f8f180a2eca4736d06dfcc533d81f45150c86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326212"
---
# <a name="shape-data-row-shape-data-section"></a>Linha Shape Data (Seção Shape Data)

Contém a informação para um único item de dados da forma associado a uma forma. Uma forma contém uma linha de dados da forma para cada item de dados da forma. As linhas de dados da forma são denominadas Prop.name e contêm as células a seguir. Para obter mais detalhes, consulte os tópicos específicos das células.
  
|**Cell**|**Descrição**|
|:-----|:-----|
|[Label](label-cell-shape-data-section.md) <br/> |Especifica o rótulo exibido aos usuários na janela ou na caixa de diálogo **Shape Data**.  <br/> |
|[Prompt](prompt-cell-shape-data-section.md) <br/> |Especifica o texto descritivo ou instrucional exibido aos usuários na janela ou na caixa de diálogo **Shape Data** quando o item é selecionado.  <br/> |
|[Tipo](type-cell-shape-data-section.md) <br/> |Especifica um tipo de dado para o valor do item de dados da forma: sequência de caracteres (0), lista fixa (1), número (2), valor booleano (3), lista variável (4), data ou hora (5), duração (6) ou moeda (7).  <br/> |
|[Format](format-cell-shape-data-section.md) <br/> |Especifica a formatação de um item de dados da forma.  <br/> |
|[Valor](value-cell-shape-data-section.md) <br/> |Contém o valor do item inserido na janela ou na caixa de diálogo **Shape Data**.  <br/> |
|[SortKey](sortkey-cell-shape-data-section.md) <br/> |Especifica uma chave pela qual os itens na janela ou na caixa de diálogo **Shape Data** são listados.  <br/> |
|[Invisible](invisible-cell-shape-data-section.md) <br/> |Especifica se o item de dados da forma será visível na janela ou na caixa de diálogo **Shape Data**. VERDADEIRO = invisível; FALSO = visível.  <br/> |
|[Feita](ask-cell-shape-data-section.md) <br/> |Determina se um usuário é solicitado a inserir as informações de dados de forma para uma forma quando uma instância é criada ou a forma é duplicada ou copiada.  <br/> |
|[LangID](langid-cell-shape-data-section.md) <br/> |Especifica o idioma em que será exibido o valor do item de dados da forma.  <br/> |
|[Calendário](calendar-cell-miscellaneous-section.md) <br/> |Especifica o tipo de calendário a ser usado quando o Tipo de um item de dados for Data.  <br/> |
   
## <a name="remarks"></a>Comentários

 Você pode adicionar tantas prop.  *nomear* linhas conforme necessário, atribuir nomes significativos às linhas e definir valores de célula. Para adicionar um item de dados da forma a uma seção Shape Data existente, clique com o botão direito do mouse em uma linha e clique em **Inserir Linha** no menu de atalho. 
  
É possível fazer referência a essas células pelo nome da linha, exibido na janela ShapeSheet em texto vermelho. Para atribuir nomes significativos à prop. *nome* , clique na linha e, em seguida, digite um nome como *Price* , por exemplo, para criar o nome da linha prop. Price. Depois, consulte a célula Label usando Prop.Price.Label. 
  
O nome de linha inserido deve ser único na seção.
  

