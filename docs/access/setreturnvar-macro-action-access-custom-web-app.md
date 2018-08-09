---
title: Ação de SetReturnVar Macro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: A ação SetReturnVar cria uma variável de retorno e o configura para um valor específico.
ms.openlocfilehash: d0638c8f1e3b184a7c685ad8649c8923bdfd8f50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765250"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a>Ação de SetReturnVar Macro (aplicativo da web personalizado do Access)

A ação **SetReturnVar** cria uma variável de retorno e o configura para um valor específico. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> A ação de **SetReturnVar** está disponível somente em Macros de dados. 
  
## <a name="setting"></a>Configuração

A ação **SetReturnVar** tem os seguintes argumentos. 
  
|**Nome do argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
| _Name_ <br/> |Sim  <br/> |Uma cadeia de caracteres que especifica o nome da variável.  <br/> |
| _Expression_ <br/> |Sim  <br/> |Uma expressão que será usada para definir o valor dessa variável temporária. Não preceda a expressão com o sinal de igual (=). Você pode clicar no botão **Construir** para usar o **Construtor de expressões** para definir este argumento.  <br/> |
   
## <a name="remarks"></a>Comentários

A ação **SetReturnVar** é usada para criar um **ReturnVar**, que é a variável que pode ser usado por macros que chamar uma macro de dados usando a ação **ExecutarMacrodeDados** . 
  
Depois que um **ReturnVar** é criado pela ação **SetReturnVar** , a macro chamada pode ser usada em uma expressão. Por exemplo, se você criou um **ReturnVar** chamado **UpdateSuccess**, você poderia usar a variável usando a seguinte sintaxe:
  
`=[ReturnVars]![UpdateSuccess]`

A ação **SetReturnVar** pode ser usada somente em macros de dados nomeada. Ele não está disponível em macros de dados que estejam anexadas a um evento de macro de dados. 
  

