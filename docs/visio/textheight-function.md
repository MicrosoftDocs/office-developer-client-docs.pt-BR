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
description: Retorna a altura do texto redigido em uma forma em que nenhuma linha de texto excede a largura máxima.
ms.openlocfilehash: 9a80dafcf80a1dcba968a0f60465aae4e2a2758b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773121"
---
# <a name="textheight-function"></a>Função TEXTHEIGHT

Retorna a altura do texto redigido em uma forma em que nenhuma linha de texto excede a _largura máxima_. 
  
## <a name="syntax"></a>Sintaxe

TEXTHEIGHT (* * *shapename! TheText* * * * * *[, largura máxima]* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _shapename! theText_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma referência à célula nomeada TheText na forma de destino.  _shapename!_ é o nome da forma do qual você deseja recuperar o texto.  <br/> |
| _largura máxima_ <br/> |Opcional  <br/> |**Numérico** <br/> |A largura máxima de um bloco de texto.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

O valor retornado inclui a altura do texto incluindo o espaço antes e após o texto, o espaçamento de linha no texto e as margens do bloco de texto superiores e inferiores. Essa função é normalmente usada para ajustar a altura de uma forma para ajustar o texto nela contido.
  
## <a name="example"></a>Exemplo

TEXTHEIGHT(TheText,(Largura - 0,5 pol)) 
  
Retorna a altura do texto quando contido na largura da forma menos 0,5 polegadas. 
  

