---
title: Função LANGUAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permite operações de comparação entre diferentes representações de idioma. Ele é melhor usado para converter os valores de marcas de idioma (BCP 47) de engenharia da Internet para valores de ID de localidade (LCID).
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327815"
---
# <a name="language-function"></a>Função LANGUAGE

Permite operações de comparação entre diferentes representações de idioma. Ele é melhor usado para converter os valores de marcas de idioma (BCP 47) de engenharia da Internet para valores de ID de localidade (LCID).
  
## <a name="version-information"></a>Informações sobre a versão

Version Added: Visio 2013
 
  
## <a name="syntax"></a>Sintaxe

 **Idioma** ( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Obrigatório  <br/> |**String** <br/> |O valor LCID ou BCP 47 para o idioma.  <br/> |
   
## <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="example"></a>Exemplo

 `LANGUAGE("en-us")`
  
Retorna um valor de ' 1033 '.
  
 `LANGUAGE("es-es")`
  
Retorna um valor de ' 3082 '.
  

