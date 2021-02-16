---
title: Armazenamento estruturado em MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f58fa70e98841db5507323a63737f1df6c1b7a6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411747"
---
# <a name="structured-storage-in-mapi"></a>Armazenamento estruturado em MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O armazenamento estruturado refere-se à organização hierárquica de armazenamento introduzida com COM. Em um ambiente de armazenamento estruturado, o armazenamento é organizado em dois ou três tipos de objetos: 
  
- Objetos Stream
    
- Bloquear objetos bytes
    
- Objetos de armazenamento
    
Bytes de fluxo e bloqueio são objetos de nível inferior que acessam diretamente os dados. Os objetos Stream implementam a interface **IStream** que define métodos de leitura, escrita, posicionamento e cópia de bytes de dados. Objetos de bytes de bloqueio implementam outra interface COM, **ILockBytes**, para acessar dados com uma matriz de bytes. Matrizes de byte são normalmente usadas para fornecer acesso personalizado ao armazenamento subjacente.
  
Objetos de armazenamento são em camadas sobre o fluxo ou objetos de bytes de bloqueio; eles podem conter um ou mais desses objetos, bem como outros objetos de armazenamento. Os objetos de armazenamento implementam a interface **IStorage** que define métodos para criar, acessar e manter objetos aninhados. 
  
Como **IStream**, **ILockBytes** e **IStorage** são interfaces COM em vez de interfaces MAPI, seus métodos retornam valores de erro COM em vez de valores MAPI. Clientes e provedores de serviços que chamam métodos nessas interfaces devem usar a função API **MapStorageSCode** para converter esses valores em valores de erro MAPI. Para obter mais informações, [consulte MapStorageSCode](mapstoragescode.md).
  
Clientes e provedores de serviços usam armazenamento estruturado para trabalhar com propriedades muito grandes para manter com os métodos **IMAPIProp,** geralmente grandes cadeias de caracteres e propriedades binárias. Uma das maneiras comuns que os clientes ou provedores de serviços acessam é especificando **IStream** ou **IStorage** como o identificador da interface em uma chamada para o método [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) Por exemplo, os clientes chamam **OpenProperty** com **PR_ATTACH_DATA_BIN** como marca de propriedade e IID_IStream identificador de interface para acessar um anexo binário em uma mensagem. 
  
Os clientes e provedores de serviços podem implementar seus próprios objetos de fluxo e armazenamento ou chamar funções de API para acessar implementações fornecidas por MAPI ou COM. Como as implementações fornecidas atendem à maioria das finalidades, os clientes e provedores de serviços raramente precisam criar seus próprios. 
  
Quando um cliente chama **OpenProperty** em um objeto MAPI para acessar uma de suas propriedades por meio de um objeto de armazenamento, o provedor de serviços normalmente abre o objeto de armazenamento no modo direto. No entanto, isso é típico em vez do comportamento necessário. Os clientes devem presumir que todos os objetos de armazenamento abertos ou criados por provedores de serviços são transacionados e exigem uma chamada para **IStorage::Commit**. Eles também devem se lembrar de que as alterações nos objetos de armazenamento não serão permanentes até **chamarem IMAPIProp::SaveChanges** após a confirmação **final** para salvar o objeto MAPI. Para obter mais informações, [consulte IMAPIProp::SaveChanges](imapiprop-savechanges.md).
  
MAPI and COM provide several API functions for defining or accessing storage and stream objects. As funções mais usadas são descritas na tabela a seguir.
  
**Funções para acessar objetos de armazenamento e fluxo**

|**Function**|**Description**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Cria um objeto de armazenamento para acessar um objeto de fluxo ou de bloqueio de bytes.  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Cria um objeto message para acessar um objeto de armazenamento.  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Cria um objeto stream para acessar um arquivo.  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Cria um objeto stream que contém a versão compactada ou descompactada de um fluxo que contém o rich text de uma mensagem.  <br/> |
   
 **Para recuperar os nomes dos fluxos em uma determinada substoragem**
  
1. Chame o método **IStorage::EnumElements** do substorage para obter uma interface **IEnumSTATSTG.** 
    
2. Chame **IEnumSTATSTG::Next** com o máximo de estruturas **STATSTG** de cada vez. Se você solicitar 100 por vez, **Next** geralmente retornará S_FALSE com o conteúdo de  _pceltFetched_ definido como o número que realmente foi recuperado. 
    
3. Verifique se há **estruturas STATSTG** sinalizadas com STGTY_STREAM. 
    
4. Libere o _parâmetro pwcsName._ 
    
 **Para criar um objeto de armazenamento para acessar um fluxo existente ou bloquear o objeto bytes**
  
- Os clientes [chamam HrIStorageFromStream](hristoragefromstream.md). 
    
 **Para criar um objeto message para acessar um objeto de armazenamento existente**
  
- Provedores de serviços e clientes chamam [OpenIMsgOnIStg](openimsgonistg.md). O objeto de mensagem criado difere dos objetos de mensagem normalmente criados pelos provedores de armazenamento de mensagens, pois ele não dá suporte a todos os métodos de interface [IMessage : IMAPIProp,](imessageimapiprop.md) como **IMessage::SubmitMessage**. Um parâmetro de entrada opcional **para OpenIMsgOnIStg** é uma função de retorno de chamada que está em conformidade com o protótipo [MSGCALLRELEASE.](msgcallrelease.md) Essa função é chamada pelo novo objeto de mensagem quando a contagem de referência da mensagem atinge zero. Implementar uma **função MSGCALLRELEASE** pode ser útil para executar o processamento final antes que a nova mensagem seja completamente removida. 
    
[OpenStreamOnFile](openstreamonfile.md) é comumente usado para armazenar anexos de arquivo porque cria um fluxo que lê e grava em um arquivo. **OpenProperty** com **PR_ATTACH_DATA_BIN** como a marca de propriedade cria um fluxo para armazenar dados de anexo binário. 
  
 **Para compactar ou descompactar um fluxo que contém o texto da mensagem no formato Rich Text**
  
- Os clientes [chamam WrapCompressedRTFStream](wrapcompressedrtfstream.md). **WrapCompressedRTFStream** cria um fluxo que quebra o fluxo RTF. O fluxo de wrapper não implementa todos os **métodos IStream;** os seguintes métodos são excluídos: **Seek**, **SetSize**, **Revert**, **LockRegion**, **UnlockRegion**, **Stat** e **Clone**. Isso porque os objetos de fluxo criados por **WrapCompressedRTFStream** não **suportam SetSize** ou **Stat**, não há uma maneira fácil de estender ou recuperar seu tamanho. A melhor estratégia é escolher um tamanho de buffer razoável e ler ou gravar em um loop.
    
> [!NOTE]
> COM tem uma implementação de objeto de armazenamento baseada em uma matriz de byte que retorna um objeto **IEnumSTATSTG** do método **EnumElements** que é problemático. Em particular, o **método QueryInterface** não funciona corretamente. Os provedores de serviços que implementam seus próprios objetos de armazenamento usando a implementação de COM devem criar um wrapper fino para o objeto **IEnumSTATSTG** que encaminha chamadas para os métodos **IEnumSTATSTG** subjacentes, mas implementa seus próprios métodos **AddRef**, **Release**, **QueryInterface** e **Clone.** 
  

