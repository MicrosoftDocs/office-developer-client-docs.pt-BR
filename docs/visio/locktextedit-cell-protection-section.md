---
title: Célula LockTextEdit (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: Protege o texto de uma forma impedindo-o de ser editado.
ms.openlocfilehash: f6e5176e3ab654b76c0641b8f642abcf6b1050dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404495"
---
# <a name="locktextedit-cell-protection-section"></a>Célula LockTextEdit (Seção Protection)

Protege o texto de uma forma impedindo-o de ser editado.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O texto não pode ser editado.  <br/> |
| FALSE  <br/> | O texto pode ser editado.  <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível formatar o texto aplicando um estilo na caixa de diálogo **Texto** (na guia **Página Inicial**, clique em na seta **Fonte**). 
  
Para obter uma referência para a célula LockTextEdit pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockTextEdit  <br/> |
   
Para obter uma referência para a célula LockTextEdit pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowLock** <br/> |
| Índice de célula:  <br/> |**visLockTextEdit** <br/> |
   

