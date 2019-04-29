---
title: Ação de macro de dados DeleteRecord (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Você pode usar a ação ExcluirRegistro para excluir um registro.
ms.openlocfilehash: 0e8a658b944e894e4d4014fb3d3d9a583efbee8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423150"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>Ação de macro de dados DeleteRecord (aplicativo Web personalizado do Access)

Você pode usar a ação **ExcluirRegistro** para excluir um registro. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A ação **DeleteRecord** tem os seguintes argumentos. 
  
|**Argumento**|**Descrição**|
|:-----|:-----|
|**Alias de Registro** <br/> |Uma cadeia de caracteres que identifica o registro a ser excluído. Se o argumento *alias* não for especificado, o registro atual será excluído.  <br/> |
   
## <a name="remarks"></a>Comentários

Você pode usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o último registro criado em um bloco de dados **CriarRegistro**. Por exemplo, use a sintaxe a seguir para fazer referência ao registro criado mais recentemente: 
  
`[LastCreateRecordIdentity]`


