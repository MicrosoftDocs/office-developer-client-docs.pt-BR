---
title: Ação de Macro ChangeView (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Você pode usar a ação ChangeView para navegar entre os modos de exibição no lugar.
ms.openlocfilehash: c420846074ef362d3388d40ed8700db0739b7ce0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765077"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>Ação de Macro ChangeView (aplicativo da web personalizado do Access)

Você pode usar a ação **ChangeView** para navegar entre os modos de exibição no lugar. 
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A ação **ChangeView** tem os seguintes argumentos. 
  
|**Argumento da ação**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
|Table  <br/> |Sim  <br/> |O nome da tabela para abrir.  <br/> |
|Exibir  <br/> |Sim  <br/> |O nome da exibição a ser aberto.  <br/> |
|Onde  <br/> |Não  <br/> |Se estiver especificado, substitui a condição Where da fonte de registro de objeto.  <br/> |
|Classificado por  <br/> |Não  <br/> |Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais. Por padrão, esse argumento estiver em branco.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Qualquer classificação ou filtragem aplicada pelo usuário é limpa quando a ação **ChangeView** é chamada. 
  
O argumento *OrderBy* é o nome do campo ou dos campos nos quais você deseja classificar os registros. Quando você usa mais de um nome de campo, separe-os com vírgula (,). 
  
Quando você define o argumento *OrderBy* , os registros são classificados por padrão em ordem crescente. 
  

