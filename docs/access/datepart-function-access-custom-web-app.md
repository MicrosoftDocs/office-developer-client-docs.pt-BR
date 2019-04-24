---
title: Função DatePart (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Retorna um valor numérico que representa a parte de data especificada da data especificada.
ms.openlocfilehash: 31ac6423614afd61ed943bb7ba375f14696df1ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280764"
---
# <a name="datepart-function-access-custom-web-app"></a>Função DatePart (aplicativo Web personalizado do Access)

Retorna um valor numérico que representa a parte de data especificada da data especificada.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**Datepart** (*Datepart*, *Data*) 
  
A função **PartData** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *DatePart*  <br/> |A parte da *Data* (um valor de data ou hora) para a qual um inteiro será retornado. Consulte a seção comentários para obter a lista de abreviações válidas.  <br/> |
| *Date*  <br/> |Uma expressão que pode ser resolvida como um valor de data/hora. A expressão de argumento de *Data* , expressão de coluna, variável definida pelo usuário ou literal de cadeia de caracteres.  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir lista todos os argumentos de *datepart* válidos. 
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**trimestre** <br/> |
|**Mês** <br/> |
|**DayOfYear** <br/> |
|**day** <br/> |
|**útil** <br/> |
|**Weekday** <br/> |
|**hora** <br/> |
|**inclusões** <br/> |
|**secundária** <br/> |
|**milissegundo** <br/> |
   

