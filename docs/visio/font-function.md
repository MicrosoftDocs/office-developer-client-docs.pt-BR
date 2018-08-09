---
title: Função FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Retorna o valor inteiro do identificador exclusivo para uma fonte, especificada por nome.
ms.openlocfilehash: 4afd2aa05f2103675bf0df8db5cc7ea21f45fe71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771919"
---
# <a name="font-function"></a>Função FONT

Retorna o valor inteiro do identificador exclusivo para uma fonte, especificada por nome.
  
> [!NOTE]
> Na maioria dos casos, o identificador de fonte é específica ao sistema. Embora a fonte permanece estabelecida uma vez usado em um arquivo, a função de **fonte** fornece acesso consistente para uma fonte específica entre sistemas e versões do Visio. É recomendável que você use a função de **fonte** para atribuir fontes em vez de referir-se diretamente aos identificadores de fonte. 
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2013
 
  
## <a name="syntax"></a>Sintaxe

 **Fonte** ( _"font_name_string"_)
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |Obrigatório  <br/> |**cadeia de caracteres** <br/> |O nome da fonte.  <br/> |
   
## <a name="return-value"></a>Valor retornado

Inteiro
  
## <a name="remarks"></a>Comentários

Se a cadeia de caracteres fornecida para *font_name_string* não corresponder a uma fonte conhecida, essa função retornará um #VALUE! erro. 
  
## <a name="example"></a>Exemplo

 `FONT("Calibri")`
  
Retorna o valor de inteiro (4) representando a ID exclusiva para a fonte "Calibri".
  

