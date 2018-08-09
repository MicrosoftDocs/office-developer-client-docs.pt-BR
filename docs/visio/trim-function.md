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
description: Remove todo o espaço do texto, com exceção de espaços simples entre palavras.
ms.openlocfilehash: b396572041e880451ceb1ec6f0508528c0807bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773188"
---
# <a name="trim-function"></a>Função TRIM

Remove todo o espaço do texto, com exceção de espaços simples entre palavras. 
  
## <a name="syntax"></a>Sintaxe

TRIM (* * *texto* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> |O texto em que os espaços devem ser removidos.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

Você pode usar a função TRIM no texto recebido de outro aplicativo que tenha espaçamento irregular.
  
## <a name="example"></a>Exemplo

TRIM ("1 de janeiro de 2003") 
  
Retornará "January 1, 2003". 
  

