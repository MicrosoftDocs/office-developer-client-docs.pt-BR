---
title: Função DateAdd (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Retorna uma data especificada com o intervalo de número especificado (inteiro positivo ou negativo) adicionada à parte dessa data data especificada.
ms.openlocfilehash: a2baa58a2ccab7d030750d03d4fddb84e8eb8ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765086"
---
# <a name="dateadd-function-access-custom-web-app"></a>Função DateAdd (aplicativo da web personalizado do Access)

Retorna uma data especificada com o intervalo de número especificado (inteiro positivo ou negativo) adicionada à parte dessa data data especificada.
  
> [!NOTE]
> O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.* > Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**DateAdd** (*DatePart*, *número*, *Data*) 
  
A função **DateAdd** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *DatePart*  <br/> |A parte da *Data* à qual um número inteiro é adicionado. Consulte a seção de comentários para a lista das configurações válidas.  <br/> |
| *Número*  <br/> |É uma expressão que possa ser resolvida para um número inteiro que é adicionado a um *DatePart* de *Data* . Se você especificar um valor com uma fração decimal, a fração será truncada.  <br/> |
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
|**hora** <br/> |
|**minuto** <br/> |
|**segundo** <br/> |
|**milissegundo** <br/> |
   
## <a name="example"></a>Example

A expressão a seguir calcula o último dia do mês atual.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

A expressão a seguir calcula o último dia do mês anterior.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


