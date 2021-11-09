# Projeto-em-delphi
projeto em delphi 
\\ estrutura básica do delphi   \\

\\ interface em delphi   \\

unit Unit4;

interface

\\ the first of all, I will create a interface. \\ 

type 

  iPeople = interface
    [ \\ code generate with acess ctlr + shift + g  \\ ]
    \\ function that generate aname of client, is the fundamental pass that create  a class \\
    function Name (Value : String : iPeople) : iPeople;
    function The_Last_name (Value : String) : iPeople;
    function NameFull : String; 
    end;

\\\\\\

type 

  TModelPeople = class(TInterfacedObject, iPeople);
  private 
    Fnone : String;
    FThe_Last_name : String;
    function Name (Value : String : iPeople) : iPeople;
    function The_Last_name (Value : String) : iPeople;
    function NameFull : String; 
  public 
    constructor Create;
    destructor Destroy; override
    \\ funcao de lasse que pode ser acessad aantes daclasse ser criada 
    class function New : iPeople;
    
  end;
  
\\ implementation of class \\

implementation


  { TModelPessoa }


end.


\\\\\\\\\\\\\\\

\\ classe 2 
constructor TModelPeople.Create;
begin

end;

destructor TModelPeople.Destroy;
begin

  inherited;
end;

class function TModelPeople.New: iPeople;
begin 
  Result := Self.Create;
end;

function TmodelPeople.name(Value : String) : iPeople;
begin 
  Result := Self;
  Fname := Value;
end;

function TModelPeople.NameFull : String;
begin 
  Result := Fnone + ' ' + Fthe_Last_name;

end; 

function TModelPeople.The_Last_name(Value : String) : iPeople;

begin 
  Result := self;
  FThe_Last_name := Value;
  
end;
\\\\\
