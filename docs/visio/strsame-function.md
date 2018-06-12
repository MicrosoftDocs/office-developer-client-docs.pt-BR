---
title: Função STRSAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
localization_priority: Normal
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: Determina se as cadeias de caracteres são os mesmos. Retornará TRUE se eles forem iguais e FALSO se forem diferentes.
ms.openlocfilehash: 5365ce6e679f708a47f4bcbdebbc4cabb13a2aee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773059"
---
# <a name="strsame-function"></a>Função STRSAME

Determina se as cadeias de caracteres são os mesmos. Retornará TRUE se eles forem iguais e FALSO se forem diferentes. 
  
## <a name="syntax"></a>Sintaxe

STRSAME ("* * *sequência1* * *","* * *sequência2* * *", * * *ignoreCase* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Sequência1_ <br/> |Obrigatório  <br/> |**String** <br/> |A primeira cadeia a ser comparada.  <br/> |
| _Sequência2_ <br/> |Obrigatório  <br/> |**String** <br/> |A segunda cadeia a ser comparada.  <br/> |
| _ignoreCase_ <br/> |Opcional  <br/> |**Boolean** <br/> |VERDADEIRO para ignorar a utilização de maiúsculas e minúsculas e FALSO para comparar a utilização. O padrão é FALSO.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Booliano
  
## <a name="remarks"></a>Comentários

Para comparar cadeias de caracteres multibyte ou para fazer comparações usando regras de maiúsculas e minúsculas para um local específico, use a função STRSAMEEX.
  
## <a name="example-1"></a>Exemplo 1

STRSAME("gato","cachorro")
  
Retornará FALSO.
  
## <a name="example-2"></a>Exemplo 2

STRSAME("gato","gato")
  
Retornará VERDADEIRO.
  
## <a name="example-3"></a>Exemplo 3

STRSAME("gato","gato", VERDADEIRO)
  
Retornará VERDADEIRO.
  
## <a name="example-4"></a>Exemplo 4

STRSAME("gato","GATO")
  
Retornará FALSO.
  
## <a name="example-5"></a>Exemplo 5

STRSAME("gato","GATO", VERDADEIRO)
  
Retornará VERDADEIRO.
  
## <a name="example-6"></a>Exemplo 6

STRSAME("gäto,"GATO", VERDADEIRO)
  
Retornará FALSO.
  
## <a name="example-7"></a>Exemplo 7

STRSAME("gäto,"GATO", VERDADEIRO)
  
Retornará VERDADEIRO.
  

