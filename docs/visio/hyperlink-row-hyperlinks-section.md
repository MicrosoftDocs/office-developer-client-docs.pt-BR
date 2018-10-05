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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390251"
---
# <a name="hyperlink-row-hyperlinks-section"></a>Linha Hyperlink (Seção Hyperlinks)

Contém as informações de um hiperlink único associado a uma forma. Uma forma conterá uma linha Hyperlink para cada hiperlink.
  
Linhas hyperlink são denominadas Hyperlink. *nome* e contém as células a seguir. Para obter mais detalhes, consulte os tópicos de célula específica. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[Descrição](description-cell-hyperlinks-section.md) <br/> |Uma sequência de caracteres descritiva para um hiperlink.  <br/> |
|[Endereço](address-cell-hyperlinks-section.md) <br/> |Um endereço URL, um nome de arquivo DOS ou um caminho UNC para o qual saltar.  <br/> |
|[Subendereço](subaddress-cell-hyperlinks-section.md) <br/> |Uma localização no documento de destino ao qual se vincular.  <br/> |
|[ExtraInfo](extrainfo-cell-hyperlinks-section.md) <br/> |Uma sequência de caracteres que passa informações a serem usadas na resolução de um URL.  <br/> |
|[Quadro](frame-cell-hyperlinks-section.md) <br/> |O nome de uma moldura para servir de destino quando o Microsoft Office Visio estiver aberto como um documento ativo em um contêiner ActiveX. O padrão é uma cadeia de caracteres vazia.  <br/> |
|[SortKey](sortkey-cell-hyperlinks-section.md) <br/> |Determina a ordem dos hiperlinks à medida que são exibidos no menu de atalho.  <br/> |
|[NewWindow](newwindow-cell-hyperlinks-section.md) <br/> |Especifica quando abrir o hiperlink em uma nova janela. Se verdadeiro, abre a página vinculada, documento ou site em uma nova janela. O padrão é FALSE.  <br/> |
|[Padrão](default-cell-hyperlinks-section.md) <br/> |O hiperlink padrão para uma forma ou página.  <br/> |
|[Invisível](invisible-cell-hyperlinks-section.md) <br/> |Indica se o hiperlink é exibido no menu de atalho.  <br/> |
   
## <a name="remarks"></a>Comentários

 Você pode adicionar tantos hiperlink.  linhas de *nome* conforme necessário, atribuir nomes significativos às linhas e definir valores de célula. Para adicionar hiperlinks a uma seção Hyperlinks existente, do mouse em uma linha e clique em **Inserir linha** no menu de atalho. 
  
Você pode fazer referência a essas células pelo nome da linha, exibido em uma janela ShapeSheet em texto vermelho. Para atribuir nomes significativos ao hiperlink. linhas de *nome* , clique na linha e digite um nome como *Marketing* , por exemplo, para criar o nome da linha Hyperlink. Você pode fazer referência à célula Description usando Hyperlink.Marketing.Description. 
  
O nome de linha inserido deve ser único na seção.
  

