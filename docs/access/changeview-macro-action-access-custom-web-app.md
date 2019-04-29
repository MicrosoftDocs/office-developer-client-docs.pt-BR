---
title: Ação de macro ChangeView (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Você pode usar a ação ChangeView para navegar entre modos de exibição no local.
ms.openlocfilehash: 0c1e27c264a826d38ec2efbd5be9bc6237ad7437
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425355"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>Ação de macro ChangeView (aplicativo Web personalizado do Access)

Você pode usar a ação **ChangeView** para navegar entre modos de exibição no local. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A ação **ChangeView** tem os seguintes argumentos. 
  
|**Argumento da ação**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
|Tabela  <br/> |Sim  <br/> |O nome da tabela que será aberta.  <br/> |
|View  <br/> |Sim  <br/> |O nome do modo de exibição que será aberto.  <br/> |
|Em que  <br/> |Não  <br/> |Se estiver especificado, substitui a condição Where da fonte de registro de objeto.  <br/> |
|Classificado Por  <br/> |Não  <br/> |Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais. Por padrão, esse argumento fica em branco.  <br/> |
   
## <a name="remarks"></a>Comentários

Qualquer classificação ou filtragem aplicada pelo usuário é desmarcada quando a ação **ChangeView** é chamada. 
  
O argumento *OrderBy* é o nome do campo ou dos campos nos quais você deseja classificar registros. Quando você usa mais de um nome de campo, separe-os com uma vírgula (,). 
  
Quando você define o argumento *OrderBy* , os registros são classificados por padrão em ordem crescente. 
  

