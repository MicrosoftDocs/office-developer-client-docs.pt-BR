---
title: Linha Hyperlink (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3065
localization_priority: Normal
ms.assetid: e3c7ae27-2e54-a174-4fb3-d16093faf759
description: Contém as informações de um hiperlink único associado a uma forma. Uma forma conterá uma linha Hyperlink para cada hiperlink.
ms.openlocfilehash: 36b9b62f248e4f5b9407156a79fa674dc2e8f14d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329901"
---
# <a name="hyperlink-row-hyperlinks-section"></a>Linha Hyperlink (Seção Hyperlinks)

Contém as informações de um hiperlink único associado a uma forma. Uma forma conterá uma linha Hyperlink para cada hiperlink.
  
As linhas Hyperlink são denominadas Hyperlink. *e*  contenha as células a seguir. Para obter mais detalhes, consulte os tópicos específicos das células. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[Descrição](description-cell-hyperlinks-section.md) <br/> |Uma sequência de caracteres descritiva para um hiperlink.  <br/> |
|[Endereço](address-cell-hyperlinks-section.md) <br/> |Um endereço URL, um nome de arquivo DOS ou um caminho UNC para o qual saltar.  <br/> |
|[SubAddress](subaddress-cell-hyperlinks-section.md) <br/> |Uma localização no documento de destino ao qual se vincular.  <br/> |
|[ExtraInfo](extrainfo-cell-hyperlinks-section.md) <br/> |Uma sequência de caracteres que passa informações a serem usadas na resolução de um URL.  <br/> |
|[Quadro](frame-cell-hyperlinks-section.md) <br/> |O nome de uma moldura para servir de destino quando o Microsoft Office Visio estiver aberto como um documento ativo em um contêiner ActiveX. O padrão é uma cadeia de caracteres vazia.  <br/> |
|[SortKey](sortkey-cell-hyperlinks-section.md) <br/> |Determina a ordem dos hiperlinks à medida que são exibidos no menu de atalho.  <br/> |
|[NewWindow](newwindow-cell-hyperlinks-section.md) <br/> |Especifica quando abrir o hiperlink em uma nova janela. Se verdadeiro, abre a página vinculada, documento ou site em uma nova janela. O padrão é FALSO.  <br/> |
|[Padrão](default-cell-hyperlinks-section.md) <br/> |O hiperlink padrão para uma forma ou página.  <br/> |
|[Invisible](invisible-cell-hyperlinks-section.md) <br/> |Indica se o hiperlink é exibido no menu de atalho.  <br/> |
   
## <a name="remarks"></a>Comentários

 É possível adicionar tantas linhas Hyperlink.  *name* quantas forem necessárias, atribuir nomes significativos às linhas e definir valores de célula. Para adicionar hiperlinks a uma seção Hyperlinks existente, clique com o botão direito do mouse em uma linha e clique em **Inserir Linha** no menu de atalho. 
  
É possível fazer referência a essas células pelo nome da linha, exibido na janela ShapeSheet em texto vermelho. Para atribuir nomes significativos às linhas Hyperlink. *name*  rows, click the row, and then type a name such as  *Marketing*  , for example, to create the row name Hyperlink.Marketing. Você pode fazer referência à célula Description usando Hyperlink.Marketing.Description. 
  
O nome de linha inserido deve ser único na seção.
  

