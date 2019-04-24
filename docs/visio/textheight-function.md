---
title: Função TEXTHEIGHT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
localization_priority: Normal
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: Retorna a altura do texto redigido em uma forma onde nenhuma linha de texto excede MaximumWidth.
ms.openlocfilehash: 7455f58f14f9a4a0ae1fcd5375dba5d5860d3852
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332319"
---
# <a name="textheight-function"></a>Função TEXTHEIGHT

Retorna a altura do texto redigido em uma forma onde nenhuma linha de texto excede _MaximumWidth_. 
  
## <a name="syntax"></a>Sintaxe

TextHEIGHT (* * *shapename! O texto* * * * * *[, MaximumWidth]* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _shapename! o texto_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma referência à célula chamada TheText na forma de destino.  _shapename!_ é o nome da forma da qual você deseja recuperar o texto.  <br/> |
| _MaximumWidth_ <br/> |Opcional  <br/> |**Numeric** <br/> |A largura máxima de um bloco de texto.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

String
  
## <a name="remarks"></a>Comentários

O valor retornado inclui a altura do texto incluindo o espaço antes e após o texto, o espaçamento de linha no texto e as margens do bloco de texto superiores e inferiores. Essa função é normalmente usada para ajustar a altura de uma forma para ajustar o texto nela contido.
  
## <a name="example"></a>Exemplo

TEXTHEIGHT(TheText,(Largura - 0,5 pol)) 
  
Retorna a altura do texto quando contido na largura da forma menos 0,5 polegadas. 
  

