---
title: Função TRIM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Remove todo o espaço do texto, exceto os espaços únicos entre as palavras.
ms.openlocfilehash: b947c9500012d0ceefe3e8044be387f7b810dda9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280840"
---
# <a name="trim-function"></a>Função TRIM

Remove todo o espaço do texto, exceto os espaços únicos entre as palavras. 
  
## <a name="syntax"></a>Sintaxe

TRIM (* * *texto* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> |O texto em que os espaços devem ser removidos.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

String
  
## <a name="remarks"></a>Comentários

Você pode usar a função TRIM no texto recebido de outro aplicativo que tenha espaçamento irregular.
  
## <a name="example"></a>Exemplo

TRIM ("1º de janeiro de 2003") 
  
Retornará "January 1, 2003". 
  

