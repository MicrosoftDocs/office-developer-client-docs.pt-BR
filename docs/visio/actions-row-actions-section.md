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
description: Contém as células que especificam as ações associadas a um comando personalizado em um menu de atalho ou de ação de marca. Seção Actions contém uma linha Actions para cada ação.
ms.openlocfilehash: f25ab75fe2bec35b09d2910ef731d11264224b7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771252"
---
# <a name="actions-row-actions-section"></a>Linha Actions (Seção Actions)

Contém as células que especificam as ações associadas a um comando personalizado em um menu de atalho ou de ação de marca. Seção Actions contém uma linha Actions para cada ação.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
As linhas Actions são denominadas Actions. *nome* e contém as células a seguir. Para obter mais detalhes, consulte os tópicos de célula específica. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[Action](action-cell-actions-section.md) <br/> |Contém a fórmula a ser executada quando o usuário escolhe um item em um menu de atalho ou de marca de ação.
  <br/> |
|[Menu](menu-cell-actions-section.md) <br/> |Define o nome do item de menu que aparece em um menu de atalho ou de marca de ação.  <br/> |
|[TagName](tagname-cell-actions-section.md) <br/> |O nome lógico da marca de ação em que essa ação deve ser exibida.  <br/> |
|[ButtonFace](buttonface-cell-actions-section.md) <br/> |Identifica o ícone exibido ao lado de um item em um menu de atalho ou de ação de marca.  <br/> |
|[SortKey](sortkey-cell-actions-section.md) <br/> |Um número que determina a ordem dos itens de menu em um menu de atalho ou de marca de ação.  <br/> |
|[Verificado](checked-cell-actions-section.md) <br/> |Indica se o item de menu é selecionado em um menu de atalho ou de marca de ação.  <br/> |
|[Desabilitado](disabled-cell-actions-section.md) <br/> |Indica se um item em um menu de atalho ou de marca de ação está desabilitado.  <br/> |
|[ReadOnly](readonly-cell-actions-section.md) <br/> |Indica se o item de menu é somente leitura (não pode ser clicado).  <br/> |
|[Invisível](invisible-cell-actions-section.md) <br/> |Indica se o item está visível no menu de atalho ou de marca de ação.  <br/> |
|[BeginGroup](begingroup-cell-actions-section.md) <br/> |Indica se deve inserir um separador no menu, acima do item de menu.  <br/> |
   
## <a name="remarks"></a>Comentários

 Você pode adicionar todas as ações.  linhas de *nome* conforme necessário, atribuir nomes significativos às linhas e definir valores de célula. Para adicionar um comando personalizado a uma seção Actions existente, do mouse em uma linha e clique em **Inserir linha** no menu de atalho. 
  
Você pode fazer referência a essas células pelo nome da linha, exibido em uma janela ShapeSheet em texto vermelho. Para atribuir um nome significativo à linha Actions. linha *nome* , clique na linha e digite um nome como *personalizado* , por exemplo, para criar o nome da linha Custom. Você pode fazer referência à célula Menu usando Actions.Custom.Menu. 
  
O nome de linha inserido deve ser único na seção.
  

