---
title: Célula GlueType (Seção Glue Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm420
localization_priority: Normal
ms.assetid: fffbefd6-8b0b-0023-6b03-026d1c6e885e
description: Determina se uma forma 1D utilizará a cola estática (ponto a ponto) ou dinâmica (forma a forma) ao ser colada em outra forma.
ms.openlocfilehash: 162827521cda6fe4a37d17a8f7d36d7a36718519
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771973"
---
# <a name="gluetype-cell-glue-info-section"></a>Célula GlueType (Seção Glue Info)

Determina se uma forma 1D utilizará a cola estática (ponto a ponto) ou dinâmica (forma a forma) ao ser colada em outra forma.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| &amp;H0  <br/> | Padrão. Permitir cola dinâmica somente para o conector dinâmico; caso contrário, utilizar cola estática.  <br/> |**visGlueTypeDefault** <br/> |
| &amp;H1  <br/> | Permitir cola dinâmica.  <br/> | Obsoleta no Visio 2002  <br/> |
| &amp;H2  <br/> | Permitir cola dinâmica.  <br/> |**visGlueTypeWalking** <br/> |
| &amp;H4  <br/> | Não permitir cola dinâmica.  <br/> |**visGlueTypeNoWalking** <br/> |
| &amp;H8  <br/> | Não permitir que esta forma 2D seja conectada com cola dinâmica.  <br/> |**visGlueTypeNoWalkingTo** <br/> |
   
## <a name="remarks"></a>Comentários

Se esta célula contiver valores de 1, 2 ou 3, a cola dinâmica será estabelecida quando um destes procedimentos ocorrer:
  
- As formas estão coladas dinamicamente na interface do usuário.
    
- As formas estão coladas nas células PinX ou PinY de outra forma a partir de um programa.
    
Se as formas estiverem coladas em células de forma diferentes de PinX ou PinY a partir de um programa, a cola estática será utilizada.
  
A alteração desse valor de permitir para não permitir a cola dinâmica não corta ou altera a cola dinâmica existente. Os programas podem estabelecer a cola dinâmica mesmo se ela estiver desabilitada na célula GlueType.
  
Para fazer referência à célula GlueType pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | GlueType  <br/> |
   
Para fazer referência à célula GlueType pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowMisc** <br/> |
| Índice da célula:  <br/> |**visGlueType** <br/> |
   

