---
title: Função LANGUAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permite operações de comparação entre representações de idiomas diferentes. Ele é melhor usado para converter valores de marcas de idioma da Internet Engineering Task Force (BCP 47) em valores de identificação de localidade (LCID).
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424747"
---
# <a name="language-function"></a>Função LANGUAGE

Permite operações de comparação entre representações de idiomas diferentes. Ele é melhor usado para converter valores de marcas de idioma da Internet Engineering Task Force (BCP 47) em valores de identificação de localidade (LCID).
  
## <a name="version-information"></a>Informações sobre a versão

Version Added: Visio 2013
 
  
## <a name="syntax"></a>Sintaxe

 **LANGUAGE**( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Obrigatório  <br/> |**String** <br/> |O valor LCID ou BCP 47 do idioma.  <br/> |
   
## <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="example"></a>Exemplo

 `LANGUAGE("en-us")`
  
Retorna um valor de '1033'.
  
 `LANGUAGE("es-es")`
  
Retorna um valor de '3082'.
  

