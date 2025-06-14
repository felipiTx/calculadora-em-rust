use std::io;

fn main() {
    println!("Calculadora simples em Rust");
    println!("Digite o primeiro número:");

    let mut num1 = String::new();
    io::stdin().read_line(&mut num1).expect("Falha ao ler entrada");
    let num1: f64 = match num1.trim().parse() {
        Ok(n) => n,
        Err(_) => {
            println!("Número inválido!");
            return;
        }
    };

    println!("Digite a operação (+, -, *, /):");
    let mut op = String::new();
    io::stdin().read_line(&mut op).expect("Falha ao ler entrada");
    let op = op.trim();

    println!("Digite o segundo número:");
    let mut num2 = String::new();
    io::stdin().read_line(&mut num2).expect("Falha ao ler entrada");
    let num2: f64 = match num2.trim().parse() {
        Ok(n) => n,
        Err(_) => {
            println!("Número inválido!");
            return;
        }
    };

    let resultado = match op {
        "+" => num1 + num2,
        "-" => num1 - num2,
        "*" => num1 * num2,
        "/" => {
            if num2 == 0.0 {
                println!("Erro: divisão por zero!");
                return;
            } else {
                num1 / num2
            }
        }
        _ => {
            println!("Operação inválida!");
            return;
        }
    };

    println!("Resultado: {}", resultado);
}
