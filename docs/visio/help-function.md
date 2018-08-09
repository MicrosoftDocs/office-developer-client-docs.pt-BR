---
title: Função HELP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
localization_priority: Normal
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: Abre um arquivo de Ajuda em HTML com a palavra-chave do especificado na caixa Pesquisar.
ms.openlocfilehash: 4671b18333bdae953c487662cd880849233df7f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772014"
---
# <a name="help-function"></a>Função HELP

Abre um arquivo de Ajuda em HTML com a *palavra-chave* do especificado na caixa **Pesquisar** . 
  
## <a name="syntax"></a>Sintaxe

AJUDAR ("* * *filename.chm!keyword* * *") 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _filename.chm!Keyword_ <br/> |Obrigatório  <br/> |**String** <br/> | O nome do arquivo da Ajuda e a palavra-chave a ser pesquisada.  <br/> |
   
## <a name="remarks"></a>Comentários

Se nenhuma *palavra-chave* for especificado, a função HELP abrirá a página de conteúdo do arquivo de Ajuda. 
  
## <a name="example"></a>Exemplo

Help("Visio.chm!ShapeSheet") 
  
Abre o arquivo da Ajuda do Visio e exibe uma lista dos tópicos cuja palavra-chave é "shapesheet". 
  

