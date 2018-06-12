---
title: Célula ViewMarkup (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Determina se a marcação é exibida na janela de desenho.
ms.openlocfilehash: dda908595b243878ec755cf73351ec1fd672dc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773272"
---
# <a name="viewmarkup-cell-document-properties-section"></a>Célula ViewMarkup (Seção Document Properties)

Determina se a marcação é exibida na janela de desenho. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A marcação é exibida no desenho.  <br/> |
|FALSO  <br/> |A marcação não é exibida (o padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

 Quando o rastreamento de marcação está ativada (a célula AddMarkup é TRUE), a célula ViewMarkup é automaticamente definida como TRUE e permanece TRUE, mesmo depois que o rastreamento de marcação foi desativada (a célula AddMarkup é FALSE). O valor da célula ViewMarkup é ignorado quando a célula AddMarkup é TRUE. 
  
A célula ViewMarkup também é definida como VERDADEIRO quando são inseridos comentários em um desenho (independente de o rastreamento de marcação estar ativado ou não) e precisa ser VERDADEIRO para que os comentários sejam exibidos no desenho.
  
Essa célula corresponde ao comando **Mostrar marcação** no grupo **marcação** na guia **revisão** . 
  
Para obter uma referência à célula ViewMarkup pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ViewMarkup  <br/> |
   
Para obter uma referência à célula ViewMarkup pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowDoc** <br/> |
|Índice da célula:  <br/> |**visDocViewMarkup** <br/> |
   

