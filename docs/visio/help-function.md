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
description: Abre um arquivo de Ajuda HTML com a palavra-chave específica na caixa Pesquisar.
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431334"
---
# <a name="help-function"></a>Função HELP

Abre um arquivo de Ajuda HTML com a palavra-chave *específica* na **caixa Pesquisar.** 
  
## <a name="syntax"></a>Sintaxe

HELP(" ** *filename.chm!keyword* ** ") 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _filename.chm!keyword_ <br/> |Obrigatório  <br/> |**String** <br/> | O nome do arquivo da Ajuda e a palavra-chave a ser pesquisada.  <br/> |
   
## <a name="remarks"></a>Comentários

Se nenhuma  *palavra-chave*  for especificada, a função HELP abrirá a página de conteúdo do arquivo de Ajuda. 
  
## <a name="example"></a>Exemplo

HELP("visio.chm!shapesheet") 
  
Abre o arquivo da Ajuda do Visio e exibe uma lista dos tópicos cuja palavra-chave é "shapesheet". 
  

