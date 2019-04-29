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
description: Determina se as cadeias de caracteres são as mesmas. Retorna TRUE se forem iguais e FALSE se não estiverem.
ms.openlocfilehash: 0f298c966ec7a3f1e23c89473fecc555ed950f79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428680"
---
# <a name="strsame-function"></a>Função STRSAME

Determina se as cadeias de caracteres são as mesmas. Retorna TRUE se forem iguais e FALSE se não estiverem. 
  
## <a name="syntax"></a>Sintaxe

STRSAME ("* * *seqüência1* * *", "* * *seqüência2* * *", * * *IgnoreCase* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |A primeira cadeia a ser comparada.  <br/> |
| _string2_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |A segunda cadeia a ser comparada.  <br/> |
| _ignoreCase_ <br/> |Opcional  <br/> |**Boolean** <br/> |VERDADEIRO para ignorar a utilização de maiúsculas e minúsculas e FALSO para comparar a utilização. O padrão é FALSO.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Booliano
  
## <a name="remarks"></a>Comentários

Para comparar cadeias de caracteres multibyte ou para fazer comparações usando regras de maiúsculas e minúsculas para um local específico, use a função STRSAMEEX.
  
## <a name="example-1"></a>Exemplo 1

STRSAME ("gato", "cachorro")
  
Retornará FALSO.
  
## <a name="example-2"></a>Exemplo 2

STRSAME ("gato", "gato")
  
Retornará VERDADEIRO.
  
## <a name="example-3"></a>Exemplo 3

STRSAME("gato","gato", VERDADEIRO)
  
Retornará VERDADEIRO.
  
## <a name="example-4"></a>Exemplo 4

STRSAME ("gato", "gato")
  
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
  

