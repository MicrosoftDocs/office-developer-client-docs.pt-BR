---
title: Dados EditarRegistro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Você pode usar o bloco de dados EditarRegistro para alterar os valores contidos em um registro existente.
ms.openlocfilehash: 6c214e48326a93cff220b5436d7e7802cd6e3431
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765057"
---
# <a name="editrecord-data-block-access-custom-web-app"></a>Dados EditarRegistro (aplicativo da web personalizado do Access)

Você pode usar o bloco de dados **EditarRegistro** para alterar os valores contidos em um registro existente. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> [!OBSERVAçãO] O bloco de dados **EditarRegistro** está disponível somente em Macros de Dados. 
  
## <a name="setting"></a>Configuração

O bloco de dados **EditarRegistro** tem os seguintes argumentos. 
  
|**Argumento**|**Descrição**|
|:-----|:-----|
|**Alias** <br/> |Uma cadeia de caracteres que identifica o registro para editar. Se o argumento *Alias* não for especificado, o registro atual é editado.  <br/> |
   
## <a name="remarks"></a>Comentários

Após a instrução **EditarRegistro** , você pode inserir um bloco de comandos que executará antes das alterações no registro forem confirmadas. As ações a seguir estão disponíveis em um bloco de dados **EditarRegistro** . 
  
||
|:-----|
|[Ação de macro CancelRecordChange](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Instrução de macro de comentário](comment-macro-block-access-custom-web-app.md) <br/> |
|[Instrução de macro de grupo](group-macro-block-access-custom-web-app.md) <br/> |
|[Se... Então... Instrução de Macro Else](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[Ação de macro SetField](setfield-macro-action-access-custom-web-app.md) <br/> |
|[Ação de macro SetLocalVar](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Use a ação **DefinirCampo** para especificar os novos valores de um campo no registro editado. 
  
Você pode usar um **se … Então... Else** instrução para executar operações com base em uma condição. 
  
Para cancelar a edição de um registro, use a ação **CancelarAlteraçãodeRegistro**. Dessa forma, as alterações não são atribuídas e o bloco de dados **EditarRegistro** é encerrado. 
  
Você pode usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o último registro criado em um bloco de dados **CriarRegistro**. Por exemplo, use a sintaxe a seguir para se referir ao campo AssignedTo do registro mais recentemente criado: 
  
`[LastCreateRecordIdentity].[AssignedTo]`


