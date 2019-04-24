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
description: Retorna uma cadeia de caracteres de imagem de formato que corresponde ao código de formato de campo de texto interno do Microsoft Visio.
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322544"
---
# <a name="fieldpicture-function"></a>Função FIELDPICTURE

Retorna uma cadeia de caracteres de imagem de formato que corresponde ao código de formato de campo de texto interno do Microsoft Visio.
  
## <a name="syntax"></a>Sintaxe

FIELDPICTURE (* * *código* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _code_ <br/> |Obrigatório  <br/> |**Número** <br/> | Um código de formato de campo de texto.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

String
  
## <a name="remarks"></a>Comentários

As sequências de caracteres de figura de formatação são utilizadas na função FORMAT para definir a expansão de valores para datas, horas, números e rótulos de unidade.
  
## <a name="example"></a>Exemplo

FIELDPICTURE (0) 
  
Retorna a cadeia de caracteres de figura de formatação "esc(0)", a qual especifica um número com uma posição decimal e uma descrição de unidade em minúsculas quando utilizada na função FORMAT. 
  

