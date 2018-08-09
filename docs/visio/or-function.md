---
title: Função OR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Retorna verdadeiro (1) se qualquer uma das expressões lógicas passadas como parâmetros forem TRUE.
ms.openlocfilehash: 14646f553e76c8c395fdbde8762daf75114f9480
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772440"
---
# <a name="or-function"></a>Função OR

Retorna verdadeiro (1) se qualquer uma das expressões lógicas passadas como parâmetros forem TRUE.
  
## <a name="syntax"></a>Sintaxe

OU (* * *expressão lógica1* * *, * * *expressão lógica2* * *,..., * * *expressão lógicaN* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão lógica1_ <br/> |Obrigatório  <br/> |**String** <br/> |A primeira expressão cuja veracidade você deseja avaliar.  <br/> |
| _expressão lógica2_ <br/> |Obrigatório  <br/> |**String** <br/> |A segunda expressão cuja veracidade você deseja avaliar.  <br/> |
| _expressão lógicaN_ <br/> |Obrigatório  <br/> |**String** <br/> |A enésima expressão cuja veracidade você deseja avaliar.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Booliano
  
## <a name="remarks"></a>Comentários

Qualquer expressão avaliada para um valor diferente de zero é considerada VERDADEIRO. Se todas as expressões lógicas forem FALSO ou iguais a 0, essa função retornará FALSO. 
  
## <a name="example"></a>Exemplo

OU (altura \> 1, PinX \> 1) 
  
Retornará VERDADEIRO (1) se qualquer uma das expressões for VERDADEIRO. Retornará FALSO (0) somente se ambas as expressões forem FALSO. 
  

