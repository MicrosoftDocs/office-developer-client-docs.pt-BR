---
title: Função FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Retorna o valor inteiro do identificador exclusivo de uma fonte, especificado por nome.
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422170"
---
# <a name="font-function"></a>Função FONT

Retorna o valor inteiro do identificador exclusivo de uma fonte, especificado por nome.
  
> [!NOTE]
> Na maioria dos casos, o identificador de fonte é específico do sistema. Embora a fonte permaneça estabelecida uma vez usada em um arquivo, a função **FONT** fornece acesso consistente a uma fonte específica entre sistemas e versões do Visio. É recomendável que você use a **função FONT** para atribuir fontes em vez de fazer referência a identificadores de fonte diretamente. 
  
## <a name="version-information"></a>Informações sobre a versão

Version Added: Visio 2013
 
  
## <a name="syntax"></a>Sintaxe

 **FONT**( _"font_name_string"_)
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |Obrigatório  <br/> |**cadeia de caracteres** <br/> |O nome da fonte.  <br/> |
   
## <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="remarks"></a>Comentários

Se a cadeia de caracteres  *fornecida font_name_string*  não corresponder a uma fonte conhecida, essa função retornará um #VALUE! . 
  
## <a name="example"></a>Exemplo

 `FONT("Calibri")`
  
Retorna o valor inteiro (4) que representa a ID exclusiva da fonte "Calibri".
  

