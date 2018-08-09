---
title: Bloco de dados CriarRegistro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Você pode usar o bloco de dados CriarRegistro para criar um novo registro na tabela especificada.
ms.openlocfilehash: dc4be7653081c7c02426d84c74b7b56e597706fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765102"
---
# <a name="createrecord-data-block-access-custom-web-app"></a>Bloco de dados CriarRegistro (aplicativo da web personalizado do Access)

Você pode usar o bloco de dados **CriarRegistro** para criar um novo registro na tabela especificada. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> [!OBSERVAçãO] O bloco de dados **CriarRegistro** está disponível somente em Macros de Dados. 
  
## <a name="setting"></a>Configuração

O bloco de dados **ExcluirRegistro** tem os seguintes argumentos. 
  
O bloco de dados **ExcluirRegistro** tem os seguintes argumentos. 
  
|**Nome do argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
|**Criar Registro em** <br/> |Sim  <br/> |O nome da tabela onde o novo registro será criado.  <br/> |
|**Alias** <br/> |Não  <br/> |Uma cadeia de caracteres que identifica o registro. Você pode usar o alias do registro para identificá-lo  <br/> |
   
## <a name="remarks"></a>Comentários

O registro criado por **CriarRegistro** se torna automaticamente o registro atual. 
  
Após a instrução **CriarRegistro** , você pode inserir um bloco de comandos que executará antes o novo registro é submetido. As ações a seguir estão disponíveis em bloco de dados **CriarRegistro**. 
  
||
|:-----|
|[Ação de macro CancelRecordChange](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Instrução de macro de comentário](comment-macro-block-access-custom-web-app.md) <br/> |
|[Instrução de macro de grupo](group-macro-block-access-custom-web-app.md) <br/> |
|[Se... Então... Instrução de Macro Else](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[Ação de macro SetField](setfield-macro-action-access-custom-web-app.md) <br/> |
|[Ação de macro SetLocalVar](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Depois que a ação **CriarRegistro** criar um registro, use a ação **DefinirCampo** para especificar o valor de um campo no novo registro. 
  
Você pode usar um **se … Então... Else** instrução para executar operações com base em uma condição. 
  
Para cancelar a criação de um registro, use a ação **CancelarAlteraçãodeRegistro**. Dessa forma, as alterações não são atribuídas e o bloco de dados **CriarRegistro** é encerrado. 
  
Quando o novo registro for atribuído, você poderá usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o registro. Por exemplo, use a sintaxe a seguir para se referir ao campo AssignedTo do registro mais recentemente criado. 
  
`[LastCreateRecordIdentity].[AssignedTo]`


