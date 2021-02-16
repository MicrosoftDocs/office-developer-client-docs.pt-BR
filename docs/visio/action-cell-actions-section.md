---
title: Célula Action (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Contém a fórmula a ser executada quando o usuário escolhe um comando em um menu de atalho ou de ação de marca.
ms.openlocfilehash: e6bc576982cad871804cbcbc5f3d9c6bceb558c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407610"
---
# <a name="action-cell-actions-section"></a>Célula Action (Seção Actions)

Contém a fórmula a ser executada quando o usuário escolhe um comando em um menu de atalho ou de ação de marca.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
## <a name="remarks"></a>Comentários

Uma célula Action é avaliada somente quando ocorre a ação, não quando a fórmula é inserida.
  
Para fazer referência à célula Action pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Ações.  *nome*  . Ação em que ações. *nome*  é o nome da linha de ações  <br/> |
   
Para fazer referência à célula Action pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionAction** <br/> |
| Índice de linha:  <br/> |**visRowAction**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visActionAction** <br/> |
   

