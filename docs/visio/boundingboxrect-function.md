---
title: Função BOUNDINGBOXRECT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Retorna a coordenada da borda especificada da caixa delimitadora da forma.
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338049"
---
# <a name="boundingboxrect-function"></a>Função BOUNDINGBOXRECT

Retorna a coordenada da borda especificada da caixa delimitadora da forma.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

BOUNDINGBOXRECT (* * *índice* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Obrigatório  <br/> |**Integer** <br/> |A borda da caixa delimitadora da forma para a qual será obtida a coordenada. Consulte Comentários para obter os valores possíveis.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

 **Número**
  
## <a name="remarks"></a>Comentários

 *Index* pode ser um dos valores a seguir. 
  
|**Item**|**Valor**|
|:-----|:-----|
|Borda esquerda  <br/> |,0  <br/> |
|Borda direita  <br/> |1  <br/> |
|Borda superior  <br/> |duas  <br/> |
|Borda inferior  <br/> |3D  <br/> |
   
Se a forma tiver um pai, o valor de retorno estará no sistema de coordenadas desse pai.
  

