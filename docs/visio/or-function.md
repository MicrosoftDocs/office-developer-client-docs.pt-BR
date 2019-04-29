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
description: Retorna TRUE (1) se qualquer uma das expressões lógicas passadas como parâmetros forem TRUE.
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433504"
---
# <a name="or-function"></a>Função OR

Retorna TRUE (1) se qualquer uma das expressões lógicas passadas como parâmetros forem TRUE.
  
## <a name="syntax"></a>Sintaxe

ou (* * *logicalexpression1* * *, * * *logicalexpression2* * *,..., * * *logicalexpressionN* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _logicalexpression1_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |A primeira expressão cuja veracidade você deseja avaliar.  <br/> |
| _logicalexpression2_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |A segunda expressão cuja veracidade você deseja avaliar.  <br/> |
| _logicalexpressionN_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |A enésima expressão cuja veracidade você deseja avaliar.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Booliano
  
## <a name="remarks"></a>Comentários

Qualquer expressão avaliada para um valor diferente de zero é considerada VERDADEIRO. Se todas as expressões lógicas forem FALSO ou iguais a 0, essa função retornará FALSO. 
  
## <a name="example"></a>Exemplo

OU (altura \> 1, PinX \> 1) 
  
Retornará VERDADEIRO (1) se qualquer uma das expressões for VERDADEIRO. Retornará FALSO (0) somente se ambas as expressões forem FALSO. 
  

