---
title: Armazenamento estruturado no MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 937643d90534f73477b90fd7ce883615a7e296f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569712"
---
# <a name="structured-storage-in-mapi"></a>Armazenamento estruturado no MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Armazenamento estruturado refere-se para a organização hierárquica de armazenamento introduzido com COM. Em um ambiente de armazenamento estruturado, o armazenamento é organizado em dois ou três tipos de objetos: 
  
- Objetos Stream
    
- Objetos de bytes de bloqueio
    
- Objetos de armazenamento
    
Stream e bloqueio bytes são objetos de nível inferior que acessem diretamente os dados. Objetos Stream implementam a interface **IStream** que define métodos para ler, gravar, posicionamento e cópia bytes de dados. Objetos de bytes de bloqueio implementar outra interface COM, **ILockBytes**, para acessar dados com uma matriz de bytes. Matrizes de byte geralmente são usados para fornecer um acesso personalizado para o armazenamento subjacente.
  
Objetos de armazenamento são colocados sobre os objetos de bytes do fluxo ou bloqueio; eles podem conter uma ou mais desses objetos, bem como outros objetos de armazenamento. Objetos de armazenamento implementam a interface de **IStorage** que define métodos para criar, acessando e manter os objetos aninhados. 
  
Como **IStream**, **ILockBytes**e **IStorage** são interfaces COM, em vez de interfaces MAPI, seus métodos retornam valores de erro COM em vez de valores MAPI. Clientes e chamar métodos nessas interfaces de provedores de serviços devem usar a função de API **MapStorageSCode** traduzir esses valores para os valores de erro MAPI. Para obter mais informações, consulte [MapStorageSCode](mapstoragescode.md).
  
Clientes e provedores de serviço usam armazenamento estruturado para trabalhar com propriedades que são grandes demais para manter-se com os métodos, normalmente grande cadeia de caracteres e propriedades binárias **IMAPIProp** . Uma das maneiras comuns que os clientes ou provedores de serviços acessá-las é especificando **IStream** ou **IStorage** como o identificador de interface em uma chamada ao método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) . Por exemplo, os clientes chamar **OpenProperty** com **PR_ATTACH_DATA_BIN** como a marca de propriedade e IID_IStream como o identificador de interface para acessar um anexo binário em uma mensagem. 
  
Clientes e provedores de serviço podem implementar seus próprios objetos stream e armazenamento ou chamar funções da API para implementações de acesso fornecidas pelo MAPI ou COM. Como as implementações fornecidas atendem a maioria das finalidades, clientes e provedores de serviços raramente precisam criar suas próprias. 
  
Quando um cliente chamadas **OpenProperty** em um objeto MAPI para acessar uma de suas propriedades por meio de um objeto de armazenamento, o provedor de serviço geralmente abrirá o objeto de armazenamento no modo direto. No entanto, isso é normal em vez de comportamento necessário. Os clientes devem pressupõem que todos os objetos de armazenamento abertos ou criados por provedores de serviços serão transacionados e exigem uma chamada para **IStorage::Commit**. Eles também devem se lembrar que as alterações em objetos de armazenamento não serão feitas permanentes até ligarem **IMAPIProp::SaveChanges** após o final **Confirmar** para salvar o objeto MAPI. Para obter mais informações, consulte [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
  
MAPI e COM fornecem várias funções de API para definir ou acessando objetos stream e armazenamento. As funções comumente usadas são descritas na tabela a seguir.
  
**Funções para acessar os objetos Stream e armazenamento**

|**Função**|**Descrição**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Cria um objeto de armazenamento para acessar um objeto de bytes do fluxo ou bloquear.  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Cria um objeto de mensagem para acessar um objeto de armazenamento.  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Cria um objeto stream para acessar um arquivo.  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Cria um objeto stream que contém a versão compactada ou descompactada de um stream mantendo o rich text de uma mensagem.  <br/> |
   
 **Para recuperar os nomes dos fluxos em um determinado subarmazenamento**
  
1. Chame o método de **IStorage::EnumElements** do subarmazenamento para obter uma interface **IEnumSTATSTG** . 
    
2. Chame **IEnumSTATSTG::Next** com quantos estruturas **STATSTG** por vez possível. Se você solicitar 100 por vez, **próximo** geralmente retornará S_FALSE com o conteúdo do _pceltFetched_ definido para o número que realmente foram recuperados. 
    
3. Verificar as estruturas **STATSTG** sinalizados com STGTY_STREAM. 
    
4. Libere o parâmetro _pwcsName_ . 
    
 **Para criar um objeto de armazenamento para acessar um objeto de bytes do fluxo ou bloqueio existente**
  
- Clientes chamar [HrIStorageFromStream](hristoragefromstream.md). 
    
 **Para criar um objeto de mensagem para acessar um objeto de armazenamento existente**
  
- Clientes e provedores de serviços de chamada [OpenIMsgOnIStg](openimsgonistg.md). O objeto de mensagem que é criado difere dos objetos de mensagem geralmente criados por provedores de armazenamento de mensagens em que ele não oferece suporte a todos os [IMessage: IMAPIProp](imessageimapiprop.md) métodos, como **IMessage::SubmitMessage**de interface. Um parâmetro de entrada opcional para **OpenIMsgOnIStg** é uma função de retorno de chamada que está em conformidade com o protótipo [MSGCALLRELEASE](msgcallrelease.md) . Essa função é chamada pelo novo objeto de mensagem quando chega a contagem de referência da mensagem zero. Implementar uma função **MSGCALLRELEASE** pode ser útil para a realização de processamento de final antes da nova mensagem será completamente removida. 
    
[OpenStreamOnFile](openstreamonfile.md) comumente é usado para armazenar os anexos de arquivo porque ele cria um fluxo que lê da e grava um arquivo. **OpenProperty** com **PR_ATTACH_DATA_BIN** como a marca de propriedade cria um fluxo para armazenar dados de anexo binário. 
  
 **Para compactar ou descompactar um stream que contém o texto da mensagem no formato Rich Text**
  
- Clientes chamar [WrapCompressedRTFStream](wrapcompressedrtfstream.md). **WrapCompressedRTFStream** cria um fluxo que envolve o fluxo RTF. O fluxo de wrapper não implementa todos os métodos **IStream** ; os métodos a seguir são excluídos: **Seek**, **SetSize**, **Reverter**, **LockRegion**, **UnlockRegion**, **Stat**e **Clone**. Isso ocorre porque os objetos stream criados pelo **WrapCompressedRTFStream** não suportam **SetSize** ou **Stat**, não há uma maneira fácil de estenda ou recuperar seu tamanho. A melhor estratégia é selecionar um tamanho de buffer razoável e ler ou gravar em um loop.
    
> [!NOTE]
> COM tem uma implementação do objeto de armazenamento com base em uma matriz de bytes que retorna um objeto **IEnumSTATSTG** pelo método **EnumElements** problemática. Em particular, o método **QueryInterface** não funciona corretamente. Provedores de serviços que implementam seus próprios objetos de armazenamento usando a implementação COM deverá criar um wrapper fino para o objeto **IEnumSTATSTG** que encaminha as chamadas para os métodos subjacentes de **IEnumSTATSTG** mas implementa seu próprio **AddRef **, Os métodos de **lançamento**, **QueryInterface**e **Clone** . 
  

