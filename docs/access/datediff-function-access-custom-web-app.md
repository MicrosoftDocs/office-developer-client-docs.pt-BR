---
title: Função DateDiff (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Retorna a contagem dos limites de parte da data especificada ultrapassados entre a data de início especificada e a data de término.
ms.openlocfilehash: fe898ec5eb59cb341250cb0c0e2e35bc55d37eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765084"
---
# <a name="datediff-function-access-custom-web-app"></a>Função DateDiff (aplicativo da web personalizado do Access)

Retorna a contagem dos limites de parte da data especificada ultrapassados entre a data de início especificada e a data de término.
  
> [!NOTE]
> O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.* > Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**DateDiff** (*DatePart*, *StartDate*, *EndDate*) 
  
A função **DateDiff** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *ParteDeData*  <br/> |É a parte da *StartDate* e *EndDate* que especifica o tipo de limite ultrapassado. Consulte a seção de comentários para a lista das configurações válidas.  <br/> |
| *StartDate*  <br/> |Uma expressão que pode ser resolvida como um valor de data/hora. A expressão de argumento *Data* , expressão de coluna, a variável definida pelo usuário ou cadeia de caracteres literal.  <br/> |
| *EndDate*  <br/> |Uma expressão que pode ser resolvida como um valor de data/hora. A expressão de argumento *Data* , expressão de coluna, a variável definida pelo usuário ou cadeia de caracteres literal.  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir lista todos os argumentos *DatePart* válidos. 
  
|***ParteDeData***|
|:-----|
|**year** <br/> |
|**trimestre** <br/> |
|**Mês** <br/> |
|**DAYOFYEAR** <br/> |
|**day** <br/> |
|**semana** <br/> |
|**hora** <br/> |
|**minuto** <br/> |
|**segundo** <br/> |
|**milissegundo** <br/> |
   

