---
title: Ação de Macro RequeryRecords (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Você pode usar a ação de RequeryRecords para atualizar, classificar e filtrar os dados no modo de exibição ativo repetindo a fonte do modo de exibição.
ms.openlocfilehash: 27c6a4f62f62f6d903de7a23d2aca6db8d316a84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765216"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>Ação de Macro RequeryRecords (aplicativo da web personalizado do Access)

Você pode usar a ação de **RequeryRecords** para atualizar, classificar e filtrar os dados no modo de exibição ativo repetindo a fonte do modo de exibição. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A ação **RequeryRecords** tem os seguintes argumentos. 
  
|**Parâmetro**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
|**Onde =** <br/> |Não  <br/> |Uma cláusula SQL WHERE que restringe os registros no modo de exibição. Por padrão, esse argumento estiver em branco.  <br/> |
|**OrderBy** <br/> |Não  <br/> |Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais. Por padrão, esse argumento estiver em branco.  <br/> |
   
## <a name="remarks"></a>Comentários

Qualquer classificação ou filtragem aplicada pelo usuário é limpa quando a ação **RequeryRecords** é chamada. 
  
O argumento *OrderBy* é o nome do campo ou dos campos nos quais você deseja classificar os registros. Quando você usa mais de um nome de campo, separe-os com vírgula (,). 
  
Quando você define o argumento *OrderBy* , os registros são classificados por padrão em ordem crescente. 
  
Para classificar registros em ordem decrescente, digite DESC no final da expressão *OrderBy* argumento. Por exemplo, para classificar registros em ordem decrescente por nome de contato do cliente, defina o argumento *OrderBy* para "ContactName DESC". 
  
Para classificar os nomes por sobrenome em ordem decrescente e FirstName crescente, defina o argumento *OrderBy* como "DESC LastName, FirstName ASC". 
  

