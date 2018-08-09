---
title: Função BOUNDINGBOXDIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Retorna a medida da parte especificada da caixa delimitadora da forma.
ms.openlocfilehash: 94cad37c4a0d2c6c7e7c69d997af09a9d7f1d651
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771425"
---
# <a name="boundingboxdist-function"></a>Função BOUNDINGBOXDIST

Retorna a medida da parte especificada da caixa delimitadora da forma. 
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

BOUNDINGBOXDIST (* * *índice* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Obrigatório  <br/> |**Número** <br/> |A parte da forma delimitadora da caixa para medir e retornar. Consulte Comentários para obter os valores possíveis.  <br/> |
   
### <a name="return-value"></a>Valor retornado

 **Número**
  
## <a name="remarks"></a>Comentários

 *Index* pode ser um dos seguintes valores. 
  
|**1.1**|**Valor**|
|:-----|:-----|
|Largura  <br/> |0  <br/> |
|Altura  <br/> |1  <br/> |
|Borda esquerda até o pino da forma  <br/> |2  <br/> |
|Pino da forma até a borda direita  <br/> |3  <br/> |
|Pino da forma até a borda superior  <br/> |4  <br/> |
|Borda inferior até o pino da forma  <br/> |5  <br/> |
|Centro da caixa delimitadora até PinX  <br/> |6  <br/> |
|Centro da caixa delimitadora até PinY  <br/> |7  <br/> |
   

