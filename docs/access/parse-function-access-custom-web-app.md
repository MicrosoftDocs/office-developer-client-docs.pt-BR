---
title: Função Analisar (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Parses a text value and returns its value in a given type using the culture of the application.
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411131"
---
# <a name="parse-function-access-custom-web-app"></a>Função Analisar (aplicativo Web personalizado do Access)

Parses a text value and returns its value in a given type using the culture of the application.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **Parse** (*TextExpression*, *DataType*) 
  
A **função Análise** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *TextExpression*  <br/> |Uma expressão de texto que representa o valor formatado a ser analisado no tipo de dados especificado.  <br/> |
| *DataType*  <br/> |Valor literal que representa o tipo de dados solicitado para o resultado.  <br/> |
   
## <a name="remarks"></a>Comentários

Use **Análise somente para** converter de tipos de cadeia de caracteres para data/hora e número. Para conversões de tipo geral, use a **função** Convert. Lembre-se de que há uma certa sobrecarga de desempenho na análise do valor da cadeia de caracteres. 
  

