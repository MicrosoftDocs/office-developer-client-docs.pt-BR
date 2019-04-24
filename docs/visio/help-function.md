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
description: Abre um arquivo de ajuda HTML com a palavra-chave especificada na caixa de pesquisa.
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329971"
---
# <a name="help-function"></a>Função HELP

Abre um arquivo de ajuda HTML com a *palavra-chave* especificada na caixa de **pesquisa** . 
  
## <a name="syntax"></a>Sintaxe

HELP ("* * *filename. chm! keyword* * *") 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _nome de arquivo. chm! palavra-chave_ <br/> |Obrigatório  <br/> |**String** <br/> | O nome do arquivo da Ajuda e a palavra-chave a ser pesquisada.  <br/> |
   
## <a name="remarks"></a>Comentários

Se nenhuma *palavra-chave* for especificada, a função ajuda abrirá a página conteúdo do arquivo de ajuda. 
  
## <a name="example"></a>Exemplo

AJUDA ("Visio. chm! ShapeSheet") 
  
Abre o arquivo da Ajuda do Visio e exibe uma lista dos tópicos cuja palavra-chave é "shapesheet". 
  

