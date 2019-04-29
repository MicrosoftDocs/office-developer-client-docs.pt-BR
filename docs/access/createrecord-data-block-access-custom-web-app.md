---
title: Bloco de dados CriarRegistro (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Você pode usar o bloco de dados CriarRegistro para criar um novo registro na tabela especificada.
ms.openlocfilehash: d89b62180dbe50a0c7dab862b70062a47558c25a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421372"
---
# <a name="createrecord-data-block-access-custom-web-app"></a>Bloco de dados CriarRegistro (aplicativo Web personalizado do Access)

Você pode usar o bloco de dados **CriarRegistro** para criar um novo registro na tabela especificada. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> O bloco de dados **CriarRegistro** está disponível somente em Macros de Dados. 
  
## <a name="setting"></a>Setting

O bloco de dados **ExcluirRegistro** tem os seguintes argumentos. 
  
O bloco de dados **ExcluirRegistro** tem os seguintes argumentos. 
  
|**Nome do argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
|**Criar Registro em** <br/> |Sim  <br/> |O nome da tabela onde o novo registro será criado.  <br/> |
|**Alias** <br/> |Não  <br/> |Uma cadeia de caracteres que identifica o registro. Você pode usar o alias do registro para identificá-lo  <br/> |
   
## <a name="remarks"></a>Comentários

O registro criado por **CriarRegistro** se torna automaticamente o registro atual. 
  
Após **** a instrução CreateRecord, você pode inserir um bloco de comandos que será executado antes que o novo registro seja confirmado. As ações a seguir estão disponíveis em bloco de dados **CriarRegistro**. 
  
||
|:-----|
|[Ação de macro CancelarAlteraçãodeRegistro](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Instrução de macro de comentário](comment-macro-block-access-custom-web-app.md) <br/> |
|[Instrução de macro de grupo](group-macro-block-access-custom-web-app.md) <br/> |
|[Instrução de macro Se...Então...Senão](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[Ação de macro SetField](setfield-macro-action-access-custom-web-app.md) <br/> |
|[Ação de macro SetLocalVar](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Depois que a ação **CriarRegistro** criar um registro, use a ação **DefinirCampo** para especificar o valor de um campo no novo registro. 
  
Você pode usar um **If... Then... Else** para executar operações com base em uma condição. 
  
Para cancelar a criação de um registro, use a ação **CancelarAlteraçãodeRegistro**. Dessa forma, as alterações não são atribuídas e o bloco de dados **CriarRegistro** é encerrado. 
  
Quando o novo registro for atribuído, você poderá usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o registro. Por exemplo, use a sintaxe a seguir para se referir ao campo AssignedTo do Registro criado mais recentemente. 
  
`[LastCreateRecordIdentity].[AssignedTo]`


