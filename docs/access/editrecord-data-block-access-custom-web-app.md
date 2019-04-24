---
title: Bloco de dados Editarregistro (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Você pode usar o bloco de dados EditarRegistro para alterar os valores contidos em um registro existente.
ms.openlocfilehash: 0d9ef6c7689b44a0304309a7537e744eff97c809
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302517"
---
# <a name="editrecord-data-block-access-custom-web-app"></a>Bloco de dados Editarregistro (aplicativo Web personalizado do Access)

Você pode usar o bloco de dados **EditarRegistro** para alterar os valores contidos em um registro existente. 
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> O bloco de dados **EditarRegistro** está disponível somente em Macros de Dados. 
  
## <a name="setting"></a>Configuração

O bloco de dados **EditarRegistro** tem os seguintes argumentos. 
  
|**Argumento**|**Descrição**|
|:-----|:-----|
|**Alias** <br/> |Uma cadeia de caracteres que identifica o registro a ser editado. Se o argumento *alias* não for especificado, o registro atual será editado.  <br/> |
   
## <a name="remarks"></a>Comentários

Após a instrução **editarregistro** , você pode inserir um bloco de comandos que será executado antes que as alterações no registro sejam confirmadas. As ações a seguir estão disponíveis em um bloco de dados **editarregistro** . 
  
||
|:-----|
|[Ação de macro CancelRecordChange](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Instrução de macro de comentário](comment-macro-block-access-custom-web-app.md) <br/> |
|[Instrução de macro de grupo](group-macro-block-access-custom-web-app.md) <br/> |
|[Instrução de macro Se...Então...Senão](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[Ação de macro SetField](setfield-macro-action-access-custom-web-app.md) <br/> |
|[Ação de macro SetLocalVar](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Use a ação **DefinirCampo** para especificar os novos valores de um campo no registro editado. 
  
Você pode usar um **If... Then... Else** para executar operações com base em uma condição. 
  
Para cancelar a edição de um registro, use a ação **CancelarAlteraçãodeRegistro**. Dessa forma, as alterações não são atribuídas e o bloco de dados **EditarRegistro** é encerrado. 
  
Você pode usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o último registro criado em um bloco de dados **CriarRegistro**. Por exemplo, use a sintaxe a seguir para se referir ao campo AssignedTo do Registro criado mais recentemente: 
  
`[LastCreateRecordIdentity].[AssignedTo]`


