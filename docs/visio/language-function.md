---
title: Função de idioma
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permite que operações de comparação entre as representações de idioma diferente. Melhor, ele é usado para conversão de valores de marcas (47 BCP) de idiomas do Internet Engineering Task Force para valores de id (LCID) da localidade.
ms.openlocfilehash: 6a05a850f5908ac5a4f6a4a72b2ce56b4c98f137
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772167"
---
# <a name="language-function"></a>Função de idioma

Permite que operações de comparação entre as representações de idioma diferente. Melhor, ele é usado para conversão de valores de marcas (47 BCP) de idiomas do Internet Engineering Task Force para valores de id (LCID) da localidade.
  
## <a name="version-information"></a>Informações da versão

Versão adicionada: Visio 2013 
  
## <a name="syntax"></a>Sintaxe

 **Idioma** ( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Obrigatório  <br/> |**String** <br/> |O valor para o idioma LCID ou 47 BCP.  <br/> |
   
## <a name="return-value"></a>Valor retornado

Inteiro
  
## <a name="example"></a>Example

 `LANGUAGE("en-us")`
  
Retorna um valor de '1033'.
  
 `LANGUAGE("es-es")`
  
Retorna um valor de '3082'.
  

