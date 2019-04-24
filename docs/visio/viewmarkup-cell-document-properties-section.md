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
ms.openlocfilehash: eeccdd0d14bf28630937b0e480822abb6fb19da5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355822"
---
# <a name="viewmarkup-cell-document-properties-section"></a>Célula ViewMarkup (Seção Document Properties)

Determina se a marcação é exibida na janela de desenho. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |A marcação é exibida no desenho.  <br/> |
|FALSE  <br/> |A marcação não é exibida (o padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

 Quando o rastreamento de marcação está ativado (a célula addMarkup é TRUE), a célula ViewMarkup é definida automaticamente como TRUE e permanece TRUE, mesmo após o rastreamento de marcação ter sido desativado (a célula addMarkup é FALSE). O valor da célula ViewMarkup é ignorado quando a célula AddMarkup está definida como VERDADEIRO. 
  
A célula ViewMarkup também é definida como VERDADEIRO quando são inseridos comentários em um desenho (independente de o rastreamento de marcação estar ativado ou não) e precisa ser VERDADEIRO para que os comentários sejam exibidos no desenho.
  
Essa célula corresponde à configuração de comando **Mostrar Marcação** no grupo **Marcação** na guia **Revisão**. 
  
Para obter uma referência à célula ViewMarkup pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ViewMarkup  <br/> |
   
Para obter uma referência para a célula ViewMarkup pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowDoc** <br/> |
|Índice da célula:  <br/> |**visDocViewMarkup** <br/> |
   

