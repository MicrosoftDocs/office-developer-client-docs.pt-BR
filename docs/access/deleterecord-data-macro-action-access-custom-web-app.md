---
title: Ação de Macro de dados ExcluirRegistro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Você pode usar a ação ExcluirRegistro para excluir um registro.
ms.openlocfilehash: 64742d73ec57b94474c8e27822fd3946c7673336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765027"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>Ação de Macro de dados ExcluirRegistro (aplicativo da web personalizado do Access)

Você pode usar a ação **ExcluirRegistro** para excluir um registro. 
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A ação **ExcluirRegistro** tem os seguintes argumentos. 
  
|**Argumento**|**Descrição**|
|:-----|:-----|
|**Alias de registro** <br/> |Uma cadeia de caracteres que identifica o registro a ser excluído. Se o argumento *Alias* não for especificado, o registro atual é excluído.  <br/> |
   
## <a name="remarks"></a>Comentários

Você pode usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o último registro criado em um bloco de dados **CriarRegistro**. Por exemplo, use a seguinte sintaxe para referir-se o registro mais recentemente criado: 
  
`[LastCreateRecordIdentity]`


