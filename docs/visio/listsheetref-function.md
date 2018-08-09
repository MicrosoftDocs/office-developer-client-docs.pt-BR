---
title: Função LISTSHEETREF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ddbc35-8577-0a96-20b8-aa7734764c5b
description: Retorna uma referência de planilha para a forma de contêiner da lista que contém a forma.
ms.openlocfilehash: 75c765fab2d287c2da83a659dbbf070d29a9d325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772242"
---
# <a name="listsheetref-function"></a>Função LISTSHEETREF

Retorna uma referência de planilha para a forma de contêiner da lista que contém a forma.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

LISTMEMBERCOUNT()
  
### <a name="return-value"></a>Valor retornado

Referência do ShapeSheet
  
## <a name="remarks"></a>Comentários

Se a forma não for um membro de lista, a função LISTSHEETREF retornará #REF!.
  
## <a name="example"></a>Exemplo

LISTSHEETREF(1)!Height 
  
Retorna o valor na célula Height da forma de contêiner da lista que contém a forma. 
  

