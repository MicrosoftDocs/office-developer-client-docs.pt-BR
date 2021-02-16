---
title: Função DatePart (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Retorna um valor numérico que representa a parte de data especificada da data especificada.
ms.openlocfilehash: 31ac6423614afd61ed943bb7ba375f14696df1ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411432"
---
# <a name="datepart-function-access-custom-web-app"></a>Função DatePart (aplicativo Web personalizado do Access)

Retorna um valor numérico que representa a parte de data especificada da data especificada.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**DatePart** (*DatePart*, *Date*) 
  
A **função DatePart** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *DatePart*  <br/> |A parte de  *Data*  (um valor de data ou hora) para a qual um inteiro será retornado. Consulte a seção Comentários para ver a lista de abreviaturas válidas.  <br/> |
| *Date*  <br/> |Uma expressão que pode ser resolvida para um valor de Data/Hora. A  *expressão do argumento Date,*  a expressão de coluna, a variável definida pelo usuário ou a cadeia de caracteres literal.  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir lista todos os  *argumentos DatePart*  válidos. 
  
|***DatePart***|
|:-----|
|**ano** <br/> |
|**quarter** <br/> |
|**Mês** <br/> |
|**dayofyear** <br/> |
|**dia** <br/> |
|**semana** <br/> |
|**weekday** <br/> |
|**hour** <br/> |
|**minuto** <br/> |
|**segundo** <br/> |
|**milissegundos** <br/> |
   

