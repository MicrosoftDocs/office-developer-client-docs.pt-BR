---
title: Função Year (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Retorna um valor numérico que representa o ano da data especificada no calendário gregoriano.
ms.openlocfilehash: 1400c352bcc070035d15b46f8e547e4637364299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433119"
---
# <a name="year-function-access-custom-web-app"></a>Função Year (aplicativo Web personalizado do Access)

Retorna um valor numérico que representa o ano da data especificada no calendário gregoriano.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **Ano** (*Data*) 
  
A função **year** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Date*  <br/> |Uma expressão que pode ser resolvida como um valor de data/hora. A expressão de argumento de *Data* , expressão de coluna, variável definida pelo usuário ou literal de cadeia de caracteres.  <br/> |
   
## <a name="remarks"></a>Comentários

Os valores retornados pelas funções **ano**, **mês**e **dia** serão valores gregorianos, independentemente do formato de exibição para o valor de data fornecido. Por exemplo, se o formato de exibição da data fornecida usar o calendário islâmico, os valores retornados para as funções **ano**, **mês**e **dia** serão valores associados à data gregoriana equivalente. 
  

