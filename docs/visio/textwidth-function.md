---
title: Função TEXTWIDTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
localization_priority: Normal
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: Retorna a largura do texto composto em uma forma.
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422030"
---
# <a name="textwidth-function"></a>Função TEXTWIDTH

Retorna a largura do texto composto em uma forma. 
  
## <a name="syntax"></a>Sintaxe

TEXTWIDTH(** *shapename! TheText* ** ** *[,maximumwidth]* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma referência à célula chamada TheText na forma de destino.  _shapename!_ é o nome da forma da qual você deseja recuperar o texto.  <br/> |
| _maximumwidth_ <br/> |Opcional  <br/> |**Numérica** <br/> |A largura máxima de um bloco de texto.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

Essa função é normalmente usada para ajustar a largura de uma forma para ajustar o texto nela contido.
  
Se  _sheetN!_ for omitida, a forma padrão será a forma atual. 
  
Se  _maximumwidth_ for especificado, o resultado é a linha de texto mais longa que se encaixa na  _maximumwidth_. Se  _maximumwidth_ for omitido, o resultado será a largura total do texto. 
  
## <a name="example"></a>Exemplo

TEXTWIDTH(TheText) 
  
Retorna o comprimento total do texto na forma atual. 
  

