# my-mbti
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MBTI로 포켓몬 찾기</title>
<style>
  :root {
    --cream: #FFF8E1;
    --cream-deep: #FFECB3;
    --yellow: #FFD54F;
    --yellow-deep: #FFB300;
    --brown: #6D4C22;
    --brown-soft: #8D6E3A;
    --white: #FFFFFF;
  }

  * { box-sizing: border-box; }

  body {
    margin: 0;
    min-height: 100vh;
    background: linear-gradient(180deg, var(--cream) 0%, var(--cream-deep) 100%);
    font-family: 'Apple SD Gothic Neo', 'Malgun Gothic', -apple-system, BlinkMacSystemFont, sans-serif;
    color: var(--brown);
    display: flex;
    justify-content: center;
    padding: 24px 16px 60px;
  }

  .wrap {
    width: 100%;
    max-width: 720px;
  }

  header {
    text-align: center;
    margin-bottom: 28px;
  }

  header h1 {
    font-size: 2.1rem;
    margin: 0 0 8px;
    color: var(--brown);
  }

  header p {
    font-size: 1.15rem;
    color: var(--brown-soft);
    margin: 0;
  }

  .card-panel {
    background: var(--white);
    border-radius: 24px;
    padding: 28px 22px;
    box-shadow: 0 8px 24px rgba(160, 120, 40, 0.15);
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 12px;
  }

  @media (max-width: 480px) {
    .grid { grid-template-columns: repeat(2, 1fr); }
    header h1 { font-size: 1.7rem; }
  }

  .mbti-btn {
    background: var(--yellow);
    border: none;
    border-radius: 16px;
    padding: 18px 8px;
    font-size: 1.3rem;
    font-weight: 800;
    color: var(--brown);
    cursor: pointer;
    transition: transform 0.15s ease, background 0.15s ease;
  }

  .mbti-btn:hover {
    background: var(--yellow-deep);
    transform: translateY(-3px) scale(1.04);
  }

  .mbti-btn:active {
    transform: scale(0.97);
  }

  .instruction {
    text-align: center;
    font-size: 1.1rem;
    margin-bottom: 18px;
    color: var(--brown-soft);
  }

  .hidden { display: none; }

  .result {
    text-align: center;
  }

  .result .type-tag {
