---
title: Linha Actions (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60017
localization_priority: Normal
ms.assetid: 29a7464a-b9d4-a8ea-161b-3044de32ed23
description: Contém células que especificam as ações associadas a um comando personalizado em um menu de atalho ou de marca de ação. A seção Actions contém uma linha Actions para cada ação.
ms.openlocfilehash: 37464e98b3e4f7d07b2ae4bd391b31ec009b6726
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408002"
---
# <a name="actions-row-actions-section"></a>Linha Actions (Seção Actions)

Contém células que especificam as ações associadas a um comando personalizado em um menu de atalho ou de marca de ação. A seção Actions contém uma linha Actions para cada ação.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
As linhas Actions são denominadas Actions. *e*  contenha as células a seguir. Para obter mais detalhes, consulte os tópicos específicos das células. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[Action](action-cell-actions-section.md) <br/> |Contém a fórmula a ser executada quando o usuário escolhe um item em um menu de atalho ou de marca de ação.  <br/> |
|[Menu](menu-cell-actions-section.md) <br/> |Define o nome do item de menu que aparece em um menu de atalho ou marca de ação.  <br/> |
|[TagName](tagname-cell-actions-section.md) <br/> |O nome lógico da marca de ação em que essa ação deve ser exibida.  <br/> |
|[ButtonFace](buttonface-cell-actions-section.md) <br/> |Identifica o ícone exibido ao lado de um item em um menu de atalho ou de marca de ação.  <br/> |
|[SortKey](sortkey-cell-actions-section.md) <br/> |Um número que determina a ordem dos itens de menu em um menu de atalho ou de marca de ação.  <br/> |
|[Verificado](checked-cell-actions-section.md) <br/> |Indica se o item de menu está marcado em um menu de atalho ou marca de ação.  <br/> |
|[Disabled](disabled-cell-actions-section.md) <br/> |Indica se um item em um menu de atalho ou de marca de ação está desabilitado.  <br/> |
|[ReadOnly](readonly-cell-actions-section.md) <br/> |Indica se o item de menu é somente leitura (não pode ser clicado).  <br/> |
|[Invisible](invisible-cell-actions-section.md) <br/> |Indica se o item está visível no menu de atalho ou de marca de ação.  <br/> |
|[BeginGroup](begingroup-cell-actions-section.md) <br/> |Indica se deve inserir um separador no menu, acima do item de menu.  <br/> |
   
## <a name="remarks"></a>Comentários

 É possível adicionar tantas linhas Actions.  *name* quantas forem necessárias, atribuir nomes significativos às linhas e definir valores de célula. Para adicionar um comando personalizado a uma seção Actions existente, clique com o botão direito do mouse em uma linha e clique em **Inserir Linha** no menu de atalho. 
  
É possível fazer referências a essas células pelo nome da linha, exibido na janela ShapeSheet em texto vermelho. Para atribuir um nome significativo à linha Actions. *linha*  de nome, clique na linha e digite um nome como  *Custom*  , por exemplo, para criar o nome da linha Actions.Custom. Você pode fazer referência à célula Menu usando Actions.Custom.Menu. 
  
O nome de linha inserido deve ser único na seção.
  

