---
title: Função STRSAMEEX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: Determina se duas cadeias de caracteres são os mesmos.
ms.openlocfilehash: 129c7429fbb3b3e5d09193b8be570045d43a0f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773081"
---
# <a name="strsameex-function"></a>Função STRSAMEEX

Determina se duas cadeias de caracteres são os mesmos.
  
## <a name="syntax"></a>Sintaxe

STRSAMEEX ("* * *sequência1* * *","* * *sequência2* * *", * * *localeID* * *, * * *sinalizador* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Sequência1_ <br/> |Obrigatório  <br/> |**String** <br/> |A primeira cadeia a ser comparada.  <br/> |
| _Sequência2_ <br/> |Obrigatório  <br/> |**String** <br/> | A segunda cadeia a ser comparada.  <br/> |
| _localeID_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O código de identificação de local.  <br/> |
| _sinalizador_ <br/> |Obrigatório  <br/> |**Numérico** <br/> | Um bit que especifica o tipo de comparação.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Booliano
  
## <a name="remarks"></a>Comentários

STRSAMEEX retornará TRUE se ambas as cadeias de caracteres de entrada são iguais e FALSE se eles não forem. Use esta função para comparar cadeias de caracteres multibyte ou para fazer comparações que usam regras de maiusculas para uma localidade específica.
  
Utilize a combinação de qualquer um dos sinalizadores a seguir com a função STRSAMEEX.
  
|**Flag**|**Descrição**|
|:-----|:-----|
|1  <br/> |Ignorar maiúsculas e minúsculas.  <br/> |
|2  <br/> |Ignorar caracteres sem espaçamento.  <br/> |
|4  <br/> |Ignorar símbolos.  <br/> |
|4096  <br/> |Tratar a pontuação da mesma forma que os símbolos.  <br/> |
|65536  <br/> |Não diferenciar entre os caracteres Hiragana e Katakana.  <br/> |
|131072  <br/> |Não diferenciar entre um caractere de byte único e o mesmo caractere como um caractere de byte duplo.  <br/> |
   

