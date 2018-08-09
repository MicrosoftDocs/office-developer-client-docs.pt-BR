---
title: Função LOWER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251459
localization_priority: Normal
ms.assetid: 1d198ea6-49e0-e462-b2cf-b65fbb920b55
description: Retorna uma cadeia de caracteres convertida em minúsculas.
ms.openlocfilehash: da626ee0bb0474fceafcf93ed5c835aacd0034fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772300"
---
# <a name="lower-function"></a>Função LOWER

Retorna uma cadeia de caracteres convertida em minúsculas.
  
## <a name="syntax"></a>Sintaxe

INFERIOR (* * *expressão* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão_ <br/> |Obrigatório  <br/> |**Varia** <br/> | Uma cadeia de caracteres, uma referência de célula ou uma expressão: o resultado é convertido em uma cadeia, que é depois convertida em minúsculas.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

A conversão de maiúsculas e minúsculas é específica a cada local, tendo por base as configurações de usuário atuais. 
  
## <a name="example"></a>Exemplo

LOWER("MAiúsculas/minÚsculas") 
  
Retornará "maiúsculas/minúsculas". 
  

