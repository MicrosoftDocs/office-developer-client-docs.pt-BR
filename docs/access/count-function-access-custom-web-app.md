---
title: Função Count (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Retorna o número de registros em uma consulta ou tabela.
ms.openlocfilehash: 300fcbfd2aa927dd19516355ae28eec2adadf521
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765081"
---
# <a name="count-function-access-custom-web-app"></a>Função Count (aplicativo da web personalizado do Access)

Retorna o número de registros em uma consulta ou tabela.
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Syntax

**Contagem** (*Expressão*) 
  
A função **Count** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Expressão*  <br/> |Uma expressão de cadeia de caracteres que identifica o campo que contém os dados que você deseja contar ou uma expressão que executa um cálculo usando os dados no campo. Operandos em *expressão* podem incluir o nome de um campo de tabela ou a função (que pode ser intrínseca ou definida pelo usuário, mas não outro SQL agregadas funções). Você pode contar qualquer tipo de dados, incluindo o texto.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Você pode usar a contagem para contar o número de registros em uma consulta de base. Por exemplo, você poderia usar contar para contar o número de pedidos enviados para um determinado país ou região.
  
**Contagem** (\*) retorna o número de itens em um grupo. Isso inclui duplicatas e valores nulos. 
  

