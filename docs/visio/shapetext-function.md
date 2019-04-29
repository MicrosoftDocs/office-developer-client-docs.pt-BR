---
title: Função SHAPETEXT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251788
localization_priority: Normal
ms.assetid: 87ea5e8f-c3e0-009f-4bf8-8c34fbdb83a6
description: Obtém o texto de uma forma.
ms.openlocfilehash: bb9b1fbe5900cd051828ed6c7ff07546567c1b23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419342"
---
# <a name="shapetext-function"></a>Função SHAPETEXT

Obtém o texto de uma forma. 
  
## <a name="syntax"></a>Sintaxe

SHAPETEXT (* * *shapename! O texto* * * * * *[, sinalizador]* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _shapename! TheText_ <br/> |Obrigatório  <br/> ||Uma referência à célula chamada TheText na forma de destino.  _Shapename!_ é o nome da forma da qual você deseja recuperar o texto.  <br/> |
| _flag_ <br/> |Opcional  <br/> |**Numérica** <br/> |Um bit que especifica o formato do texto. O sinalizador padrão (0) mostra o texto exatamente como está na forma.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

Utilize a combinação de qualquer um dos sinalizadores a seguir com a função STRSAMEEX.
  
|**Flag**|**Descrição**|
|:-----|:-----|
|,0  <br/> |Mostrar o texto exatamente como está na forma.  <br/> |
|1  <br/> |Incluir hífens discricionários.  <br/> |
|duas  <br/> |Não incluir texto expandido nos campos.  <br/> |
|4   <br/> |Converter tabulações em espaços simples.  <br/> |
|8   <br/> |Converter tabulações em um conjunto de espaços.  <br/> |
|16   <br/> |Converter retornos de texto e alimentação de linhas em espaços.  <br/> |
|32  <br/> |Converter aspas tipográficas em aspas normais.  <br/> |
|64  <br/> |Converter espaços em branco adjacentes em um espaço simples.  <br/> |
   
## <a name="example-1"></a>Exemplo 1

SHAPETEXT (planilha! texto)
  
Retornará o texto da forma sheetN exatamente como está na forma.
  
## <a name="example-2"></a>Exemplo 2

SHAPETEXT (o texto)
  
Retornará o texto da forma atual exatamente como está na forma.
  
## <a name="example-3"></a>Exemplo 3

SHAPETEXT(theText, 84)
  
Retornará o texto da forma atual. Converterá também espaço em branco adjacente em espaço simples (64), retornos de texto e alimentação de linhas em espaços (16) e tabulações em espaço simples (4). A soma desses sinalizadores é 84.
  

