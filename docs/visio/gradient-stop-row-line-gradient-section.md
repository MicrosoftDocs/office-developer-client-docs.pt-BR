---
title: Linha de parada de gradiente (seção line Gradient)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1236a59e-2a25-449f-8e20-8553518d79ec
description: Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de linha.
ms.openlocfilehash: 1a6d9c60bc83160067123007cf873c5681e9bc85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360253"
---
# <a name="gradient-stop-row-line-gradient-section"></a>Linha de parada de gradiente (seção line Gradient)

Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de linha.
  
Uma linha de **parada** de gradiente contém as células a seguir. 
  
|**Cell**|**Descrição**|
|:-----|:-----|
|**Color** <br/> |O valor de cor da marca de gradiente. Esse valor pode ser expresso como o número de índice de uma cor na paleta de documentos ou usando as funções [RGB](rgb-function-visioshapesheet.md), [THEMEVAL](themeval-function.md)ou [HSL](hsl-function.md) (por exemplo).  <br/> |
|**ColorTrans** <br/> |A quantidade de transparência da cor do gradiente, como uma porcentagem.  <br/> |
|**Posição** <br/> |A posição da parada do gradiente ao longo da direção do gradiente de linha, como uma porcentagem do ponto de origem do gradiente para a borda externa da linha.  <br/> |
   

