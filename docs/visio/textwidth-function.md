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
description: Retorna a largura do texto redigido em uma forma.
ms.openlocfilehash: d96b9489c08ce38205f8e9ad91e361fcb643c39c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773119"
---
# <a name="textwidth-function"></a>Função TEXTWIDTH

Retorna a largura do texto redigido em uma forma. 
  
## <a name="syntax"></a>Sintaxe

TEXTWIDTH (* * *shapename! TheText* * * * * *[, largura máxima]* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _shapename! theText_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma referência à célula nomeada TheText na forma de destino.  _shapename!_ é o nome da forma do qual você deseja recuperar o texto.  <br/> |
| _largura máxima_ <br/> |Opcional  <br/> |**Numérico** <br/> |A largura máxima de um bloco de texto.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

Essa função é normalmente usada para ajustar a largura de uma forma para ajustar o texto nela contido.
  
Se _sheetN!_ for omitido, a forma padrão será a forma atual. 
  
Se a _largura máxima_ for especificado, o resultado é a linha mais longa do texto que caiba na _largura máxima_. Se a _largura máxima_ for omitido, o resultado é a largura total do texto. 
  
## <a name="example"></a>Exemplo

TextWidth(TheText) 
  
Retorna o comprimento total do texto na forma atual. 
  

