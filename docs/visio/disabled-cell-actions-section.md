---
title: Célula Disabled (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: Indica se um item em um menu de atalho ou de marca de ação está desabilitado.
ms.openlocfilehash: 3956b6cf5ccb870255d6943e74b4f02650952d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771714"
---
# <a name="disabled-cell-actions-section"></a>Célula Disabled (Seção Actions)

Indica se um item em um menu de atalho ou de marca de ação está desabilitado.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Desativar (esmaecer) o nome do comando.  <br/> |
|FALSO  <br/> |Ativar o nome do comando (padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula Disabled pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome* . Desabilitado onde ações. *nome* é o nome da linha Actions  <br/> |
   
Para obter uma referência para a célula Disabled pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice da linha:  <br/> |**visRowAction** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visActionDisabled** <br/> |
   

