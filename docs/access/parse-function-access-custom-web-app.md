---
title: Analisar a função (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analisa um valor de texto e retorna seu valor em um determinado tipo usando a cultura do aplicativo.
ms.openlocfilehash: fa3c453f1faeadca173aaace513ee5ba9115c5fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765208"
---
# <a name="parse-function-access-custom-web-app"></a>Analisar a função (aplicativo da web personalizado do Access)

Analisa um valor de texto e retorna seu valor em um determinado tipo usando a cultura do aplicativo.
  
> [!NOTE]
> O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.* > Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **Analisar** (*TextExpression*, *DataType*) 
  
A função **Analisar** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Uma expressão de texto representando o valor formatado para analisar em tipo de dados especificado.  <br/> |
| *Tipo de dados*  <br/> |Valor literal que representa o tipo de dados solicitado para o resultado.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Use a **Analisar** apenas para a conversão de cadeia de caracteres, data/hora e tipos de número. Para conversões de tipo geral, use a função **Converter** . Tenha em mente que há um determinado desempenho sobrecarga na análise o valor de cadeia de caracteres. 
  

