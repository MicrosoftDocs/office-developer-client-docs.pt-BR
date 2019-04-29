---
title: Ação de macro Repetirconsultaderegistros (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Você pode usar a ação Repetirconsultaderegistros para atualizar, classificar e filtrar os dados no modo de exibição ativo, consultando novamente a fonte do modo de exibição.
ms.openlocfilehash: 69d88401abc0de417f7dc58e275c66f2037212aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439244"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>Ação de macro Repetirconsultaderegistros (aplicativo Web personalizado do Access)

Você pode usar a ação **repetirconsultaderegistros** para atualizar, classificar e filtrar os dados no modo de exibição ativo, consultando novamente a fonte do modo de exibição. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A ação **repetirconsultaderegistros** tem os seguintes argumentos. 
  
|**Parâmetro**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
|**Onde =** <br/> |Não  <br/> |Uma cláusula SQL WHERE que restringe os registros no modo de exibição. Por padrão, esse argumento fica em branco.  <br/> |
|**OrderBy** <br/> |Não  <br/> |Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais. Por padrão, esse argumento fica em branco.  <br/> |
   
## <a name="remarks"></a>Comentários

Qualquer classificação ou filtragem aplicada pelo usuário é desmarcada quando a ação **repetirconsultaderegistros** é chamada. 
  
O argumento *OrderBy* é o nome do campo ou dos campos nos quais você deseja classificar registros. Quando você usa mais de um nome de campo, separe-os com uma vírgula (,). 
  
Quando você define o argumento *OrderBy* , os registros são classificados por padrão em ordem crescente. 
  
Para classificar registros em ordem decrescente, insira DESC no final da expressão de argumento *OrderBy* . Por exemplo, para classificar registros de cliente em ordem decrescente por nome de contato, defina o argumento *OrderBy* como "ContactName desc". 
  
Para classificar nomes por LastName Descending e FirstName Ascending, defina o argumento *OrderBy* como "LastName DESC, FirstName ASC". 
  

