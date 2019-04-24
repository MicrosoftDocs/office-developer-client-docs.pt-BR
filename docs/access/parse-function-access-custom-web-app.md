---
title: Função Parse (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analisa um valor de texto e retorna seu valor em um determinado tipo usando a cultura do aplicativo.
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308054"
---
# <a name="parse-function-access-custom-web-app"></a>Função Parse (aplicativo Web personalizado do Access)

Analisa um valor de texto e retorna seu valor em um determinado tipo usando a cultura do aplicativo.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **Parse** (*Texté*, *DataType*) 
  
A função **Parse** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *TextExpression*  <br/> |Uma expressão de texto representando o valor formatado para analisar o tipo de dados especificado.  <br/> |
| *DataType*  <br/> |Valor literal que representa o tipo de dados solicitado para o resultado.  <br/> |
   
## <a name="remarks"></a>Comentários

Use **Parse** somente para conversão de cadeia de caracteres para tipos de data/hora e de número. Para conversões de tipo gerais, use a função **Convert** . Tenha em mente que há uma certa sobrecarga de desempenho na análise do valor da cadeia de caracteres. 
  

