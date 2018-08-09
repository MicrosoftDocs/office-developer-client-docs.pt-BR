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
ms.openlocfilehash: 53a0cb6e485ae2fd233792e1ebd9765426b7f798
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772931"
---
# <a name="shapetext-function"></a>Função SHAPETEXT

Obtém o texto de uma forma. 
  
## <a name="syntax"></a>Sintaxe

STRSAMEEX (* * *shapename! TheText* * * * * *[, sinalizador]* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _shapename! TheText_ <br/> |Obrigatório  <br/> ||Uma referência à célula nomeada TheText na forma de destino.  _Shapename!_ é o nome da forma do qual você deseja recuperar o texto.  <br/> |
| _sinalizador_ <br/> |Opcional  <br/> |**Numérico** <br/> |Um bit que especifica o formato do texto. O sinalizador padrão (0) mostra o texto exatamente como está na forma.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

Utilize a combinação de qualquer um dos sinalizadores a seguir com a função STRSAMEEX.
  
|**Flag**|**Descrição**|
|:-----|:-----|
|0  <br/> |Mostrar o texto exatamente como está na forma.  <br/> |
|1  <br/> |Incluir hífens discricionários.  <br/> |
|2  <br/> |Não incluir texto expandido nos campos.  <br/> |
|4  <br/> |Converter tabulações em espaços simples.  <br/> |
|8  <br/> |Converter tabulações em um conjunto de espaços.  <br/> |
|16  <br/> |Converter retornos de texto e alimentação de linhas em espaços.  <br/> |
|32  <br/> |Converter aspas tipográficas em aspas normais.  <br/> |
|64  <br/> |Converter espaços em branco adjacentes em um espaço simples.  <br/> |
   
## <a name="example-1"></a>Exemplo 1

SHAPETEXT(sheetN!theText)
  
Retornará o texto da forma sheetN exatamente como está na forma.
  
## <a name="example-2"></a>Exemplo 2

SHAPETEXT(theText)
  
Retornará o texto da forma atual exatamente como está na forma.
  
## <a name="example-3"></a>Exemplo 3

SHAPETEXT(theText, 84)
  
Retornará o texto da forma atual. Converterá também espaço em branco adjacente em espaço simples (64), retornos de texto e alimentação de linhas em espaços (16) e tabulações em espaço simples (4). A soma desses sinalizadores é 84.
  

