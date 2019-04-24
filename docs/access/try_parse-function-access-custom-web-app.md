---
title: Função Try_Parse (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analisa um valor de texto para o tipo de dados especificado na cultura do aplicativo ou retorna NULL se a conversão não for válida.
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307795"
---
# <a name="tryparse-function-access-custom-web-app"></a>Função Try_Parse (aplicativo Web personalizado do Access)

Analisa um valor de texto para o tipo de dados especificado na cultura do aplicativo ou retorna NULL se a conversão não for válida.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **Try_Parse** (*Texté*, *DataType*) 
  
A função **Try_Parse** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *TextExpression*  <br/> |Uma expressão de texto representando o valor formatado para analisar o tipo de dados especificado.  <br/> |
| *DataType*  <br/> |O tipo de dados no qual a *textName* será analisada.  <br/> |
   
## <a name="remarks"></a>Comentários

Use **Try_Parse** somente para conversão de cadeia de caracteres para tipos de data/hora e de número. Para conversões de tipo gerais, continue a usar **Convert**. 
  

