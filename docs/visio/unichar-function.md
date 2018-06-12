---
title: Função UNICHAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Retorna o caractere Unicode de um número.
ms.openlocfilehash: 06f97717ee4d5965253b0da7cfd5c35faf0ca2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773219"
---
# <a name="unichar-function"></a>Função UNICHAR

Retorna o caractere Unicode de um número. 
  
## <a name="syntax"></a>Sintaxe

UNICHAR (* * *número* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Integer** <br/> |Um número inteiro entre 1 e 65.535 (inclusive) ou a função retornará um erro.  <br/> |
   
## <a name="remarks"></a>Comentários

A cadeia de caracteres resultante é um caractere Unicode (dois caracteres). 
  
## <a name="example"></a>Example

UNICHAR(65) 
  
Retorna um (letra latina A maiuscula) 
  

