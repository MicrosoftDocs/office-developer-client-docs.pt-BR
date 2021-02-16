---
title: Try_Parse (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analisará um valor de texto para o tipo de dados especificado na cultura do aplicativo ou retornará Null se a conversão não for válida.
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427525"
---
# <a name="try_parse-function-access-custom-web-app"></a>Try_Parse (aplicativo Web personalizado do Access)

Analisará um valor de texto para o tipo de dados especificado na cultura do aplicativo ou retornará Null se a conversão não for válida.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **Try_Parse** (*TextExpression*, *DataType*) 
  
A **Try_Parse** função contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *TextExpression*  <br/> |Uma expressão de texto que representa o valor formatado a ser analisado no tipo de dados especificado.  <br/> |
| *DataType*  <br/> |O tipo de dados no qual analisar  *TextExpression*  .  <br/> |
   
## <a name="remarks"></a>Comentários

Use **Try_Parse** somente para converter de tipos de cadeia de caracteres para data/hora e número. Para conversões de tipo geral, continue a usar **Convert**. 
  

