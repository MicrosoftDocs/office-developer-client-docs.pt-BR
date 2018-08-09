---
title: Função Try_Parse (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analisa um valor de texto para o tipo de dados especificado na cultura do aplicativo ou retorna Null se a conversão não é válida.
ms.openlocfilehash: 3446e928d9772641f9aea7b956e142f995824b1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765248"
---
# <a name="tryparse-function-access-custom-web-app"></a>Função Try_Parse (aplicativo da web personalizado do Access)

Analisa um valor de texto para o tipo de dados especificado na cultura do aplicativo ou retorna Null se a conversão não é válida.
  
> [!NOTE]
> O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.* > Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **Try_Parse** (*TextExpression*, *DataType*) 
  
A função **Try_Parse** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *TextExpression*  <br/> |Uma expressão de texto representando o valor formatado para analisar em tipo de dados especificado.  <br/> |
| *DataType*  <br/> |O tipo de dados no qual analisar *TextExpression* .  <br/> |
   
## <a name="remarks"></a>Comentários

Use **Try_Parse** apenas para a conversão de cadeia de caracteres, data/hora e tipos de número. Para conversões de tipo geral, continue a usar a **Converter**. 
  

