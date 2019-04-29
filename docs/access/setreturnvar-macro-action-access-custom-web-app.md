---
title: Ação de macro SetReturnVar (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: A ação SetReturnVar cria uma variável de retorno e a define como um valor específico.
ms.openlocfilehash: 29445f5021bed99fe45cee1d34457f1f91ca417d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409591"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a>Ação de macro SetReturnVar (aplicativo Web personalizado do Access)

A ação **SetReturnVar** cria uma variável de retorno e a define como um valor específico. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> A ação **SetReturnVar** está disponível somente em macros de dados. 
  
## <a name="setting"></a>Setting

A ação **SetReturnVar** tem os seguintes argumentos. 
  
|**Nome do argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
| _Nome_ <br/> |Sim  <br/> |Uma cadeia de caracteres que especifica o nome da variável.  <br/> |
| _Expressão_. <br/> |Sim  <br/> |Uma expressão que será usada para definir o valor dessa variável temporária. Não preceda a expressão com o sinal de igualdade (=). Você pode clicar no botão **Build** para usar o **Construtor de Expressões** para definir esse argumento.  <br/> |
   
## <a name="remarks"></a>Comentários

A ação **SetReturnVar** é usada para criar um **ReturnVar**, que é variável que pode ser usada por macros que chamam uma macro de dados usando a ação **RunDataMacro** . 
  
Depois que um **ReturnVar** é criado pela ação **SetReturnVar** , a macro de chamada pode usá-la em uma expressão. Por exemplo, se você criou um **ReturnVar** chamado **UpdateSuccess**, poderia usar a variável usando a seguinte sintaxe:
  
`=[ReturnVars]![UpdateSuccess]`

A ação **SetReturnVar** pode ser usada somente em macros de dados nomeadas. Ele não está disponível em macros de dados anexadas a um evento de macro de dados. 
  

