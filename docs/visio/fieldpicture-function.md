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
description: Retorna uma cadeia de caracteres de figura de formatação que coincida com o código de formato de campo de texto interno do Microsoft Visio.
ms.openlocfilehash: 1528cefd65ed0c7c1dde02fa390babf26442b4d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771843"
---
# <a name="fieldpicture-function"></a>Função FIELDPICTURE

Retorna uma cadeia de caracteres de figura de formatação que coincida com o código de formato de campo de texto interno do Microsoft Visio.
  
## <a name="syntax"></a>Sintaxe

FIELDPICTURE (* * *código* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _code_ <br/> |Obrigatório  <br/> |**Número** <br/> | Um código de formato de campo de texto.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

As sequências de caracteres de figura de formatação são utilizadas na função FORMAT para definir a expansão de valores para datas, horas, números e rótulos de unidade.
  
## <a name="example"></a>Exemplo

FIELDPICTURE(0) 
  
Retorna a cadeia de caracteres de figura de formatação "esc(0)", a qual especifica um número com uma posição decimal e uma descrição de unidade em minúsculas quando utilizada na função FORMAT. 
  

