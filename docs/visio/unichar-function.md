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
ms.openlocfilehash: 81e76b72da35f79dee9ad6afbde51bc2e228483c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417578"
---
# <a name="unichar-function"></a>Função UNICHAR

Retorna o caractere Unicode de um número. 
  
## <a name="syntax"></a>Sintaxe

UNICHAR (* * *número* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Integer** <br/> |Um número inteiro entre 1 e 65.535 (inclusive) ou a função retornará um erro.  <br/> |
   
## <a name="remarks"></a>Comentários

A cadeia de caracteres resultante é um caractere Unicode (dois caracteres). 
  
## <a name="example"></a>Exemplo

UNICHAR (65) 
  
Retorna A (letra latina maiúscula A) 
  

