---
title: Função BOUNDINGBOXDIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Retorna a medida da parte especificada da caixa delimitadora da forma.
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348962"
---
# <a name="boundingboxdist-function"></a>Função BOUNDINGBOXDIST

Retorna a medida da parte especificada da caixa delimitadora da forma. 
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

BOUNDINGBOXDIST (* * *índice* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Obrigatório  <br/> |**Número** <br/> |A parte da caixa delimitadora da forma para medir e retornar. Consulte comentários para os valores possíveis.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

 **Número**
  
## <a name="remarks"></a>Comentários

 *Index* pode ser um dos valores a seguir. 
  
|**Item**|**Valor**|
|:-----|:-----|
|Largura  <br/> |,0  <br/> |
|Altura  <br/> |1  <br/> |
|Borda esquerda até o pino da forma  <br/> |duas  <br/> |
|Pino da forma até a borda direita  <br/> |3D  <br/> |
|Pino da forma até a borda superior  <br/> |quatro  <br/> |
|Borda inferior até o pino da forma  <br/> |0,5  <br/> |
|Centro da caixa delimitadora até PinX  <br/> |6  <br/> |
|Centro da caixa delimitadora até PinY  <br/> |178  <br/> |
   

