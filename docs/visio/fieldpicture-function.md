---
title: Função FIELDPICTURE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
localization_priority: Normal
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Retorna uma cadeia de caracteres de formatação que corresponde ao código de formato de campo de texto interno do Microsoft Visio.
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431453"
---
# <a name="fieldpicture-function"></a>Função FIELDPICTURE

Retorna uma cadeia de caracteres de formatação que corresponde ao código de formato de campo de texto interno do Microsoft Visio.
  
## <a name="syntax"></a>Sintaxe

FIELDPICTURE(** *code* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _code_ <br/> |Obrigatório  <br/> |**Número** <br/> | Um código de formato de campo de texto.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

As sequências de caracteres de figura de formatação são utilizadas na função FORMAT para definir a expansão de valores para datas, horas, números e rótulos de unidade.
  
## <a name="example"></a>Exemplo

FIELDPICTURE(0) 
  
Retorna a cadeia de caracteres de figura de formatação "esc(0)", a qual especifica um número com uma posição decimal e uma descrição de unidade em minúsculas quando utilizada na função FORMAT. 
  

