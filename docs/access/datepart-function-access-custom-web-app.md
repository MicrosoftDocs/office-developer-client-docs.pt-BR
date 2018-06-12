---
title: Função DatePart (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Retorna um valor numérico que representa a parte da data especificada da data especificada.
ms.openlocfilehash: 81aa1880e5b38c33f75018418a44ed82e5e7e8c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765042"
---
# <a name="datepart-function-access-custom-web-app"></a>Função DatePart (aplicativo da web personalizado do Access)

Retorna um valor numérico que representa a parte da data especificada da data especificada.
  
> [!NOTE]
> O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.* > Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**DatePart** (*DatePart*, *Data*) 
  
A função **PartData** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *DatePart*  <br/> |A parte de *Data* (um valor de data ou hora) para o qual será retornado um número inteiro. Consulte a seção de comentários para a lista de abreviações válidas.  <br/> |
| *Date*  <br/> |Uma expressão que pode ser resolvida como um valor de data/hora. A expressão de argumento *Data* , expressão de coluna, a variável definida pelo usuário ou cadeia de caracteres literal.  <br/> |
   
## <a name="remarks"></a>Coment�rios

A tabela a seguir lista todos os argumentos *DatePart* válidos. 
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**trimestre** <br/> |
|**Mês** <br/> |
|**DAYOFYEAR** <br/> |
|**day** <br/> |
|**semana** <br/> |
|**Weekday** <br/> |
|**hora** <br/> |
|**minuto** <br/> |
|**segundo** <br/> |
|**milissegundo** <br/> |
   

