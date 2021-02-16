---
title: Função DateDiff (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Retorna a contagem dos limites da parte de data especificados cruzados entre a data de início e a data de término especificadas.
ms.openlocfilehash: 1cce8a501c5a57384372e681f903baa4f4c20bef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415611"
---
# <a name="datediff-function-access-custom-web-app"></a>Função DateDiff (aplicativo Web personalizado do Access)

Retorna a contagem dos limites da parte de data especificados cruzados entre a data de início e a data de término especificadas.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**DateDiff** (*DatePart*, *StartDate*, *EndDate*) 
  
A **função DateDiff** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *DatePart*  <br/> |É a parte de  *StartDate*  *e EndDate*  que especifica o tipo de limite cruzado. Consulte a seção Comentários para ver a lista de configurações válidas.  <br/> |
| *StartDate*  <br/> |Uma expressão que pode ser resolvida para um valor de Data/Hora. A  *expressão do argumento Date,*  a expressão de coluna, a variável definida pelo usuário ou a cadeia de caracteres literal.  <br/> |
| *EndDate*  <br/> |Uma expressão que pode ser resolvida para um valor de Data/Hora. A  *expressão do argumento Date,*  a expressão de coluna, a variável definida pelo usuário ou a cadeia de caracteres literal.  <br/> |
   
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
|**hour** <br/> |
|**minute** <br/> |
|**segundo** <br/> |
|**milissegundos** <br/> |
   

