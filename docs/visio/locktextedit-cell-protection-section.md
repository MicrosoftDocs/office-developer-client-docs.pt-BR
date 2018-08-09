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
ms.openlocfilehash: 7f8800f0b260e808a46ec123d27784f3dd92e847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772268"
---
# <a name="locktextedit-cell-protection-section"></a>Célula LockTextEdit (Seção Protection)

Protege o texto de uma forma impedindo-o de ser editado.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O texto não pode ser editado.  <br/> |
| FALSO  <br/> | O texto pode ser editado.  <br/> |
   
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
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockTextEdit** <br/> |
   

