<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>M-PVC</title>

  <style>

    /* =========================================================
       기본 설정
    ========================================================== */

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: "Pretendard", "Noto Sans KR", Arial, sans-serif;
      background: #f5f5f3;
      color: #111;
    }

    img {
      display: block;
      max-width: 100%;
    }



    /* =========================================================
       01 / M-PVC INTRO
    ========================================================== */

    .mpvc-intro {
      min-height: 100vh;
      display: flex;
      align-items: center;
      position: relative;
      overflow: hidden;

      background:
        radial-gradient(
          circle at 80% 45%,
          rgba(185, 190, 187, 0.22),
          transparent 35%
        ),
        #f5f5f3;
    }

    .mpvc-inner {
      width: min(1400px, calc(100% - 120px));
      margin: 0 auto;
      position: relative;
      z-index: 2;
      padding: 100px 0;
    }

    .mpvc-label {
      display: flex;
      align-items: center;
      gap: 18px;
      margin-bottom: 42px;
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 3px;
      color: #777;
    }

    .mpvc-label::before {
      content: "";
      width: 48px;
      height: 1px;
      background: #999;
      flex-shrink: 0;
    }

    .mpvc-title {
      font-size: clamp(76px, 11vw, 175px);
      font-weight: 500;
      letter-spacing: -8px;
      line-height: 0.85;
    }

    .mpvc-title span {
      color: #9a9a96;
      font-weight: 300;
    }

    .mpvc-headline {
      margin-top: 65px;
      max-width: 1000px;
      font-size: clamp(30px, 3.5vw, 54px);
      font-weight: 400;
      line-height: 1.3;
      letter-spacing: -2.5px;
      word-break: keep-all;
    }

    .mpvc-headline strong {
      font-weight: 650;
    }

    .mpvc-description-wrap {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 80px;
      margin-top: 70px;
      padding-top: 38px;
      border-top: 1px solid #cfcfcb;
    }

    .mpvc-section-label {
      display: flex;
      align-items: center;
      gap: 18px;
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 3px;
      color: #777;
    }

    .mpvc-section-label::before {
      content: "";
      width: 48px;
      height: 1px;
      background: #999;
      flex-shrink: 0;
    }

    .mpvc-description-image {
      display: block;
      width: 100%;
      max-width: 500px;
      height: auto;
      margin-top: 35px;
      object-fit: contain;
    }

    .mpvc-description {
      max-width: 620px;
      font-size: 17px;
      line-height: 1.95;
      color: #666;
      word-break: keep-all;
    }

    .mpvc-description strong {
      color: #111;
      font-weight: 600;
    }

    .mpvc-side-text {
      position: absolute;
      right: 34px;
      top: 50%;
      transform: translateY(-50%) rotate(90deg);
      transform-origin: center;
      font-size: 10px;
      letter-spacing: 4px;
      color: #aaa;
      white-space: nowrap;
    }

    .scroll-down {
      position: absolute;
      right: 6%;
      bottom: 45px;
      display: flex;
      align-items: center;
      gap: 15px;
      font-size: 10px;
      letter-spacing: 2px;
      color: #888;
    }

    .scroll-down span {
      display: block;
      width: 55px;
      height: 1px;
      background: #999;
    }



    /* =========================================================
       02 / WHY M-PVC
    ========================================================== */

    .mpvc-compare {
      padding: 150px 0;
      background: #111;
      color: #fff;
    }

    .compare-inner {
      width: min(1400px, calc(100% - 120px));
      margin: 0 auto;
    }

    .compare-label {
      display: flex;
      align-items: center;
      gap: 18px;
      margin-bottom: 55px;
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 3px;
      color: #777;
    }

    .compare-label::before {
      content: "";
      width: 48px;
      height: 1px;
      background: #555;
      flex-shrink: 0;
    }

    .compare-head {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 100px;
      align-items: end;
    }

    .compare-head h2 {
      font-size: clamp(48px, 6vw, 90px);
      line-height: 1;
      letter-spacing: -4px;
      font-weight: 450;
    }

    .compare-head p {
      max-width: 600px;
      color: #999;
      line-height: 1.9;
      font-size: 17px;
      word-break: keep-all;
    }


    .material-compare {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      margin-top: 100px;
      border-top: 1px solid #333;
      border-bottom: 1px solid #333;
    }

    .material-card {
      padding: 45px 40px 55px;
      border-right: 1px solid rgba(0,0,0,0.12);
      min-width: 0;
      color: #111;
    }

    .material-card:last-child {
      border-right: none;
    }

    .material-card:nth-child(1) {
      background: #ffffff;
    }

    .material-card:nth-child(2) {
      background: #d8c6aa;
    }

    .material-card-m {
      background: #D7DEE0;
      color: #111;
    }

    .material-top {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      font-size: 10px;
      letter-spacing: 2px;
      color: #666;
    }

    .material-card h3 {
      margin-top: 45px;
      font-size: clamp(42px, 5vw, 72px);
      font-weight: 400;
      letter-spacing: -3px;
      color: #111;
    }

    .material-image {
      height: 280px;
      margin: 45px 0 35px;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }

    .material-image img {
      width: 140%;
      height: 140%;
      max-width: none;
      object-fit: contain;
    }

    .material-name {
      font-size: 12px;
      font-weight: 600;
      letter-spacing: 2px;
      margin-bottom: 20px;
      color: #111;
    }

    .material-card p {
      color: #4d4d4d;
      line-height: 1.9;
      font-size: 15px;
      word-break: keep-all;
    }

    .mpvc-combination {
      margin-top: 35px;
      padding-top: 25px;
      border-top: 1px solid rgba(0,0,0,0.18);
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 15px;
      font-size: 11px;
      letter-spacing: 1px;
      color: #111;
    }

    .mpvc-combination strong {
      font-size: 22px;
      font-weight: 300;
    }


    .compare-table {
      margin-top: 100px;
      border-top: 1px solid #444;
    }

    .compare-row {
      display: grid;
      grid-template-columns: 1.3fr 1fr 1fr 1fr;
      border-bottom: 1px solid #2d2d2d;
    }

    .compare-row > div {
      padding: 24px 20px;
      font-size: 14px;
      color: #aaa;
    }

    .compare-row-head > div {
      color: #fff;
      font-size: 13px;
      font-weight: 600;
      letter-spacing: 1px;
    }

    .compare-category {
      color: #fff !important;
    }

    .compare-row .highlight {
      color: #111;
      background: #D7DEE0;
      font-weight: 600;
    }

    .compare-final {
      margin-top: 130px;
      padding-top: 50px;
      border-top: 1px solid #333;
    }

    .compare-final span {
      font-size: 11px;
      letter-spacing: 3px;
      color: #777;
    }

    .compare-final h3 {
      margin-top: 30px;
      font-size: clamp(42px, 5.5vw, 78px);
      font-weight: 350;
      line-height: 1.18;
      letter-spacing: -3px;
    }



    /* =========================================================
       03 / WHY BETTER
    ========================================================== */

    .mpvc-benefits {
      padding: 150px 0;
      background: #f5f5f3;
      color: #111;
    }

    .benefits-inner {
      width: min(1400px, calc(100% - 120px));
      margin: 0 auto;
    }

    .benefits-label {
      display: flex;
      align-items: center;
      gap: 18px;
      margin-bottom: 55px;
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 3px;
      color: #777;
    }

    .benefits-label::before {
      content: "";
      width: 48px;
      height: 1px;
      background: #999;
      flex-shrink: 0;
    }

    .benefits-head {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 100px;
      align-items: end;
    }

    .benefits-head h2 {
      font-size: clamp(48px, 6vw, 88px);
      font-weight: 450;
      line-height: 1.08;
      letter-spacing: -4px;
    }

    .benefits-head p {
      max-width: 580px;
      font-size: 17px;
      line-height: 1.9;
      color: #666;
      word-break: keep-all;
    }

    .benefits-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      margin-top: 100px;
      border-top: 1px solid #cfcfcb;
      border-left: 1px solid #cfcfcb;
    }

    .benefit-card {
      min-height: 560px;
      padding: 35px 45px 50px;
      border-right: 1px solid #cfcfcb;
      border-bottom: 1px solid #cfcfcb;
      display: flex;
      flex-direction: column;
      position: relative;
      transition: background 0.3s ease;
    }

    .benefit-card:hover {
      background: #fff;
    }

    .benefit-top {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
      font-size: 10px;
      letter-spacing: 2px;
      color: #888;
    }

    .benefit-icon {
      width: 150px;
      height: 150px;
      margin-top: 60px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .benefit-icon img {
      width: 125px;
      height: 125px;
      object-fit: contain;
    }

    .benefit-content {
      margin-top: auto;
      padding-top: 55px;
    }

    .benefit-en {
      margin-bottom: 12px;
      font-size: 10px;
      font-weight: 600;
      letter-spacing: 2.5px;
      color: #888;
    }

    .benefit-content h3 {
      font-size: clamp(30px, 3vw, 45px);
      font-weight: 500;
      letter-spacing: -2px;
      line-height: 1.2;
    }

    .benefit-content p {
      max-width: 500px;
      margin-top: 22px;
      font-size: 15px;
      line-height: 1.9;
      color: #666;
      word-break: keep-all;
    }

    .benefit-card-wide {
      grid-column: 1 / -1;
      min-height: 470px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-template-rows: auto 1fr;
      column-gap: 80px;
    }

    .benefit-card-wide .benefit-top {
      grid-column: 1 / -1;
    }

    .benefit-card-wide .benefit-icon {
      width: 180px;
      height: 180px;
      margin-top: 60px;
    }

    .benefit-card-wide .benefit-icon img {
      width: 150px;
      height: 150px;
    }

    .benefit-card-wide .benefit-content {
      margin-top: 0;
      padding-top: 60px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }



    /* =========================================================
       04 / M-PVC STRUCTURE
    ========================================================== */

    .mpvc-structure {
      padding: 150px 0;
      background: #111;
      color: #fff;
    }

    .structure-inner {
      width: min(1400px, calc(100% - 120px));
      margin: 0 auto;
    }

    .structure-label {
      display: flex;
      align-items: center;
      gap: 18px;
      margin-bottom: 55px;
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 3px;
      color: #777;
    }

    .structure-label::before {
      content: "";
      width: 48px;
      height: 1px;
      background: #555;
      flex-shrink: 0;
    }

    .structure-head {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 100px;
      align-items: end;
    }

    .structure-head h2 {
      font-size: clamp(48px, 6vw, 88px);
      font-weight: 400;
      line-height: 1.05;
      letter-spacing: -4px;
    }

    .structure-head p {
      max-width: 580px;
      font-size: 17px;
      line-height: 1.9;
      color: #999;
      word-break: keep-all;
    }

    .structure-types {
      display: grid;
      grid-template-columns: 1fr 1fr;
      margin-top: 100px;
      border-top: 1px solid #333;
      border-bottom: 1px solid #333;
    }

    .structure-type {
      padding: 45px 45px 60px;
      min-width: 0;
    }

    .structure-type:first-child {
      border-right: 1px solid #333;
    }

    .structure-type-top {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      font-size: 10px;
      letter-spacing: 2px;
      color: #777;
    }

    .structure-type h3 {
      margin-top: 38px;
      font-size: clamp(60px, 7vw, 100px);
      font-weight: 300;
      letter-spacing: -4px;
      line-height: 1;
    }

    .structure-type h3 span {
      margin-left: 15px;
      font-size: 14px;
      font-weight: 500;
      letter-spacing: 2px;
      color: #777;
    }

    .structure-profile {
      height: 570px;
      margin-top: 35px;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }

    .structure-profile img {
      width: 110%;
      height: 110%;
      max-width: none;
      object-fit: contain;
    }

    .structure-info {
      padding-top: 35px;
      border-top: 1px solid #333;
    }

    .structure-info-label {
      font-size: 10px;
      font-weight: 600;
      letter-spacing: 2.5px;
      color: #777;
    }

    .structure-info h4 {
      margin-top: 15px;
      font-size: 28px;
      font-weight: 500;
      letter-spacing: -1.5px;
    }

    .structure-info p {
      max-width: 500px;
      margin-top: 20px;
      font-size: 15px;
      line-height: 1.9;
      color: #999;
      word-break: keep-all;
    }

    .structure-bottom {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 100px;
      margin-top: 100px;
      padding-top: 45px;
      border-top: 1px solid #333;
    }

    .structure-bottom-small {
      font-size: 11px;
      letter-spacing: 3px;
      color: #777;
    }

    .structure-bottom h3 {
      margin-top: 18px;
      font-size: clamp(34px, 4vw, 58px);
      font-weight: 350;
      line-height: 1.2;
      letter-spacing: -2px;
    }

    .structure-bottom p {
      max-width: 580px;
      font-size: 15px;
      line-height: 1.9;
      color: #999;
      word-break: keep-all;
    }



    /* =========================================================
       05 / PERFORMANCE
    ========================================================== */

    .mpvc-performance {
      padding: 150px 0;
      background: #f5f5f3;
      color: #111;
    }

    .performance-inner {
      width: min(1400px, calc(100% - 120px));
      margin: 0 auto;
    }

    .performance-label {
      display: flex;
      align-items: center;
      gap: 18px;
      margin-bottom: 55px;
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 3px;
      color: #777;
    }

    .performance-label::before {
      content: "";
      width: 48px;
      height: 1px;
      background: #999;
      flex-shrink: 0;
    }

    .performance-head {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 100px;
      align-items: end;
    }

    .performance-head h2 {
      font-size: clamp(48px, 6vw, 88px);
      font-weight: 450;
      line-height: 1.08;
      letter-spacing: -4px;
    }

    .performance-head p {
      max-width: 580px;
      font-size: 17px;
      line-height: 1.9;
      color: #666;
      word-break: keep-all;
    }


    /* 열관류율 / 차음 */

    .performance-block {
      display: grid;
      grid-template-columns: 1.55fr 0.75fr;
      gap: 140px;
      align-items: center;

      min-height: 600px;
      margin-top: 110px;
      padding: 70px 0;

      border-top: 1px solid #cfcfcb;
    }

    .performance-block-reverse {
      grid-template-columns: 0.75fr 1.55fr;
    }

    .performance-number-wrap {
      min-width: 0;
    }

    .performance-index {
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 2.5px;
      color: #888;
    }

    .performance-big-number {
      margin-top: 45px;
      font-size: clamp(85px, 9vw, 145px);
      font-weight: 300;
      line-height: 0.95;
      letter-spacing: -7px;
      white-space: nowrap;
    }

    .performance-big-number span {
      display: inline-block;
      margin: 0 10px;
      color: #999;
      font-weight: 200;
    }

    .performance-unit {
      margin-top: 25px;
      font-size: 18px;
      font-weight: 500;
      letter-spacing: 1px;
      color: #666;
    }

    .performance-info {
      max-width: 520px;
    }

    .performance-en {
      margin-bottom: 15px;
      font-size: 10px;
      font-weight: 600;
      letter-spacing: 2.5px;
      color: #888;
    }

    .performance-info h3 {
      font-size: clamp(36px, 4vw, 58px);
      font-weight: 500;
      letter-spacing: -2px;
      line-height: 1.15;
    }

    .performance-info p {
      margin-top: 28px;
      font-size: 16px;
      line-height: 1.9;
      color: #666;
      word-break: keep-all;
    }


    /* 결로 */

    .performance-condensation {
      margin-top: 60px;
      padding-top: 80px;
      border-top: 1px solid #cfcfcb;
    }

    .condensation-top {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 100px;
      align-items: end;
    }

    .condensation-top h3 {
      margin-top: 35px;
      font-size: clamp(58px, 7vw, 105px);
      font-weight: 350;
      line-height: 1;
      letter-spacing: -5px;
    }

    .condensation-top h4 {
      font-size: 38px;
      font-weight: 500;
      letter-spacing: -2px;
    }

    .condensation-top p {
      max-width: 540px;
      margin-top: 25px;
      font-size: 16px;
      line-height: 1.9;
      color: #666;
      word-break: keep-all;
    }

    .condensation-values {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      margin-top: 90px;
      border-top: 1px solid #cfcfcb;
      border-left: 1px solid #cfcfcb;
    }

    .condensation-item {
      min-height: 280px;
      padding: 35px;
      border-right: 1px solid #cfcfcb;
      border-bottom: 1px solid #cfcfcb;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .condensation-name {
      font-size: 13px;
      font-weight: 500;
      color: #666;
    }

    .condensation-number {
      margin-top: 45px;
      font-size: clamp(48px, 6vw, 84px);
      font-weight: 350;
      letter-spacing: -4px;
    }

    .condensation-bottom {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 50px;
      margin-top: 40px;
      padding-top: 30px;
      border-top: 1px solid #cfcfcb;
    }

    .condensation-bottom span {
      font-size: 10px;
      letter-spacing: 3px;
      color: #888;
    }

    .condensation-bottom strong {
      font-size: 18px;
      font-weight: 500;
      letter-spacing: -0.5px;
    }



    /* =========================================================
       모바일
    ========================================================== */


    /* =========================================================
       06 / PRODUCT LINE-UP
    ========================================================== */

    .mpvc-products {
      background: #f5f5f3;
      color: #111;
    }

    .products-intro {
      background: #f5f5f3;
    }

    .products-inner,
    .product-inner,
    .special-inner {
      width: min(1400px, calc(100% - 120px));
      margin: 0 auto;
    }

    .products-inner {
      padding: 150px 0 130px;
    }

    .products-label {
      display: flex;
      align-items: center;
      gap: 18px;
      margin-bottom: 55px;
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 3px;
      color: #777;
    }

    .products-label::before {
      content: "";
      width: 48px;
      height: 1px;
      background: #999;
      flex-shrink: 0;
    }

    .products-head {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 100px;
      align-items: end;
    }

    .products-head h2 {
      font-size: clamp(48px, 6vw, 88px);
      font-weight: 450;
      line-height: 1.07;
      letter-spacing: -4px;
    }

    .products-head p {
      max-width: 580px;
      font-size: 17px;
      line-height: 1.9;
      color: #666;
      word-break: keep-all;
    }

    .product-section {
      padding: 100px 0 130px;
    }

    .product-light { background: #f5f5f3; }
    .product-white { background: #fff; }

    .product-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      padding-bottom: 35px;
      border-bottom: 1px solid #bdbdb8;
    }

    .product-number {
      display: flex;
      align-items: flex-end;
      gap: 20px;
    }

    .product-number span {
      margin-bottom: 12px;
      font-size: 10px;
      letter-spacing: 3px;
      color: #888;
    }

    .product-number strong {
      font-size: clamp(70px, 8vw, 120px);
      line-height: .8;
      font-weight: 300;
      letter-spacing: -6px;
    }

    .product-type { text-align: right; }

    .product-type span {
      display: block;
      margin-bottom: 10px;
      font-size: 10px;
      letter-spacing: 2.5px;
      color: #888;
    }

    .product-type strong {
      font-size: 15px;
      font-weight: 600;
      letter-spacing: 2px;
    }

    .product-profile-area {
      display: grid;
      grid-template-columns: .8fr 1.5fr .7fr;
      gap: 60px;
      align-items: center;
      min-height: 600px;
      padding: 70px 0;
    }

    .product-profile-title span,
    .product-size > span,
    .application-head span {
      font-size: 10px;
      font-weight: 600;
      letter-spacing: 3px;
      color: #888;
    }

    .product-profile-title h3,
    .application-head h3 {
      margin-top: 20px;
      font-size: clamp(30px, 3.5vw, 50px);
      font-weight: 450;
      line-height: 1.2;
      letter-spacing: -2px;
      word-break: keep-all;
    }

    .product-profile-image {
      height: 470px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .product-profile-image img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }

    .product-size { text-align: right; }
    .product-size > span { display: block; margin-bottom: 22px; }
    .product-size-value { white-space: nowrap; }

    .product-size strong {
      font-size: clamp(70px, 8vw, 120px);
      font-weight: 300;
      line-height: .85;
      letter-spacing: -6px;
    }

    .product-size em {
      margin-left: 8px;
      font-size: 18px;
      font-style: normal;
      color: #777;
    }

    .product-inner-divider {
      width: 100%;
      height: 1px;
      background: #cfcfcb;
      margin: 20px 0 70px;
    }

    .application-head {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 100px;
      align-items: end;
      margin-bottom: 45px;
    }

    .application-head span { display: block; margin-bottom: 16px; }

    .application-head p {
      max-width: 430px;
      justify-self: end;
      font-size: 15px;
      line-height: 1.8;
      color: #666;
      word-break: keep-all;
    }

    .application-image {
      width: 100%;
      height: clamp(500px, 60vw, 820px);
      overflow: hidden;
      background: #e8e8e5;
    }

    .application-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .product-main-divider {
      position: relative;
      width: 100%;
      height: 8px;
      background: #111;
    }

    .product-main-divider span {
      position: absolute;
      right: 60px;
      top: 18px;
      font-size: 9px;
      font-weight: 600;
      letter-spacing: 3px;
      color: #999;
    }

    .special-product {
      background: #111;
      color: #fff;
      padding: 160px 0 170px;
    }

    .special-label {
      display: flex;
      align-items: center;
      gap: 18px;
      margin-bottom: 55px;
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 3px;
      color: #888;
    }

    .special-label::before {
      content: "";
      width: 48px;
      height: 1px;
      background: #666;
    }

    .special-head {
      display: grid;
      grid-template-columns: 1.15fr .85fr;
      gap: 100px;
      align-items: end;
    }

    .special-head > h2 {
      font-size: clamp(60px, 8vw, 120px);
      font-weight: 300;
      line-height: .88;
      letter-spacing: -6px;
    }

    .special-description > span,
    .fire-test-head span,
    .fire-lineup-head span,
    .fire-product-info > span,
    .fire-size span {
      display: block;
      font-size: 10px;
      letter-spacing: 3px;
      color: #777;
    }

    .special-description > span { margin-bottom: 20px; }

    .special-description h3 {
      font-size: clamp(30px, 3.5vw, 50px);
      font-weight: 400;
      line-height: 1.25;
      letter-spacing: -2px;
    }

    .special-description p {
      max-width: 500px;
      margin-top: 25px;
      font-size: 15px;
      line-height: 1.9;
      color: #999;
      word-break: keep-all;
    }

    .fire-test {
      margin-top: 120px;
      padding-top: 50px;
      border-top: 1px solid #333;
    }

    .fire-test-head {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      margin-bottom: 45px;
    }

    .fire-test-head span { margin-bottom: 14px; }

    .fire-test-head h3 {
      font-size: clamp(32px, 4vw, 55px);
      font-weight: 400;
      letter-spacing: -2px;
    }

    .fire-test-number {
      font-size: 11px;
      letter-spacing: 4px;
      color: #666;
    }

    .fire-test-image {
      width: 100%;
      height: clamp(550px, 65vw, 900px);
      overflow: hidden;
      background: #1b1b1b;
    }

    .fire-test-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .fire-lineup {
      margin-top: 130px;
      padding-top: 55px;
      border-top: 1px solid #333;
    }

    .fire-lineup-head span { margin-bottom: 15px; }

    .fire-lineup-head h3 {
      font-size: clamp(38px, 5vw, 65px);
      font-weight: 350;
      letter-spacing: -3px;
    }

    .fire-products {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      margin-top: 65px;
      border-top: 1px solid #333;
      border-bottom: 1px solid #333;
    }

    .fire-product {
      position: relative;
      padding: 35px 40px 50px;
      min-width: 0;
      border-right: 1px solid #333;
    }

    .fire-product:last-child { border-right: none; }

    .fire-product-number {
      font-size: 11px;
      letter-spacing: 3px;
      color: #777;
    }

    .fire-product-image {
      height: 400px;
      margin: 40px 0;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .fire-product-image img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }

    .fire-product-info {
      padding-top: 30px;
      border-top: 1px solid #333;
    }

    .fire-product-info > span { margin-bottom: 12px; }

    .fire-product-info h4 {
      font-size: 28px;
      font-weight: 400;
      letter-spacing: -1px;
    }

    .fire-size { margin-top: 45px; }
    .fire-size span { margin-bottom: 14px; font-size: 9px; }

    .fire-size strong {
      font-size: 55px;
      font-weight: 300;
      letter-spacing: -3px;
    }

    .fire-size em {
      margin-left: 6px;
      font-size: 15px;
      font-style: normal;
      color: #777;
    }




    /* =========================================================
       PRODUCT 01~04 / H · F PROFILE
    ========================================================== */

    .product-profile-area.product-profile-hf {
      grid-template-columns: .62fr 2.38fr;
      gap: 70px;
      align-items: center;
    }

    .profile-variants {
      display: grid;
      grid-template-columns: 1fr 1fr;
      min-width: 0;
    }

    .profile-variant {
      position: relative;
      min-width: 0;
      padding: 0 52px;
    }

    .profile-variant + .profile-variant {
      border-left: 1px solid #d2d2ce;
    }

    .profile-variant-image {
      height: 430px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .profile-variant-image img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }

    .profile-variant-info {
      margin-top: 34px;
      padding-top: 22px;
      border-top: 1px solid #d2d2ce;
    }

    .variant-type {
      margin-bottom: 22px;
      font-size: 11px;
      font-weight: 600;
      letter-spacing: 3px;
      color: #111;
    }

    .variant-width-label {
      margin-bottom: 9px;
      font-size: 9px;
      font-weight: 500;
      letter-spacing: 2.5px;
      color: #888;
    }

    .variant-width {
      display: flex;
      align-items: baseline;
      gap: 8px;
    }

    .variant-width strong {
      font-size: 42px;
      font-weight: 350;
      line-height: 1;
      letter-spacing: -2px;
    }

    .variant-width span {
      font-size: 13px;
      color: #777;
    }


    @media (max-width: 900px) {

      .mpvc-inner,
      .compare-inner,
      .benefits-inner,
      .structure-inner,
      .performance-inner {
        width: calc(100% - 40px);
      }

      .mpvc-intro {
        min-height: auto;
      }

      .mpvc-inner {
        padding: 100px 0;
      }

      .mpvc-title {
        font-size: clamp(65px, 20vw, 120px);
        letter-spacing: -5px;
      }

      .mpvc-headline {
        margin-top: 45px;
        font-size: 32px;
      }

      .mpvc-description-wrap {
        grid-template-columns: 1fr;
        gap: 35px;
        margin-top: 50px;
      }

      .mpvc-description-image {
        max-width: 100%;
      }

      .mpvc-side-text,
      .scroll-down {
        display: none;
      }


      /* 02 */

      .mpvc-compare {
        padding: 100px 0;
      }

      .compare-head {
        grid-template-columns: 1fr;
        gap: 35px;
      }

      .material-compare {
        grid-template-columns: 1fr;
        margin-top: 70px;
      }

      .material-card {
        border-right: none;
        border-bottom: 1px solid rgba(0,0,0,0.12);
      }

      .material-image {
        height: 220px;
      }

      .compare-table {
        overflow-x: auto;
      }

      .compare-row {
        min-width: 700px;
      }

      .compare-final {
        margin-top: 90px;
      }


      /* 03 */

      .mpvc-benefits {
        padding: 100px 0;
      }

      .benefits-head {
        grid-template-columns: 1fr;
        gap: 35px;
      }

      .benefits-grid {
        grid-template-columns: 1fr;
        margin-top: 70px;
      }

      .benefit-card {
        min-height: 500px;
        padding: 30px 25px 40px;
      }

      .benefit-card-wide {
        grid-column: auto;
        display: flex;
        min-height: 500px;
      }

      .benefit-card-wide .benefit-content {
        margin-top: auto;
        padding-top: 45px;
      }


      /* 04 */

      .mpvc-structure {
        padding: 100px 0;
      }

      .structure-head {
        grid-template-columns: 1fr;
        gap: 35px;
      }

      .structure-types {
        grid-template-columns: 1fr;
        margin-top: 70px;
      }

      .structure-type {
        padding: 35px 25px 50px;
      }

      .structure-type:first-child {
        border-right: none;
        border-bottom: 1px solid #333;
      }

      .structure-profile {
        height: 390px;
      }

      .structure-profile img {
        width: 105%;
        height: 105%;
      }

      .structure-bottom {
        grid-template-columns: 1fr;
        gap: 35px;
        margin-top: 70px;
      }


      /* 05 */

      .mpvc-performance {
        padding: 100px 0;
      }

      .performance-head {
        grid-template-columns: 1fr;
        gap: 35px;
      }

      .performance-block,
      .performance-block-reverse {
        grid-template-columns: 1fr;
        min-height: auto;
        gap: 50px;
        margin-top: 70px;
        padding: 60px 0;
      }

      .performance-big-number {
        font-size: clamp(65px, 18vw, 110px);
        letter-spacing: -5px;
      }

      .performance-block-reverse .performance-info {
        order: 2;
      }

      .performance-block-reverse .performance-number-wrap {
        order: 1;
      }

      .performance-condensation {
        margin-top: 40px;
        padding-top: 60px;
      }

      .condensation-top {
        grid-template-columns: 1fr;
        gap: 50px;
      }

      .condensation-values {
        grid-template-columns: 1fr;
        margin-top: 60px;
      }

      .condensation-item {
        min-height: 220px;
      }

      .condensation-bottom {
        flex-direction: column;
        align-items: flex-start;
        gap: 18px;
      }


      /* 06 */

      .products-inner,
      .product-inner,
      .special-inner {
        width: calc(100% - 40px);
      }

      .products-inner { padding: 100px 0 80px; }

      .products-head,
      .application-head,
      .special-head {
        grid-template-columns: 1fr;
        gap: 35px;
      }

      .product-section { padding: 75px 0 90px; }

      .product-header { align-items: flex-start; }

      .product-number { display: block; }
      .product-number span { display: block; margin-bottom: 20px; }
      .product-number strong { font-size: 70px; }
      .product-type strong { font-size: 11px; }

      .product-profile-area {
        grid-template-columns: 1fr;
        gap: 35px;
        min-height: auto;
        padding: 60px 0;
      }

      .product-profile-image { height: 350px; }

      .product-size {
        text-align: left;
        padding-top: 30px;
        border-top: 1px solid #d5d5d1;
      }

      .product-size strong { font-size: 75px; }
      .application-head p { justify-self: start; }
      .application-image { height: 450px; }
      .product-main-divider { height: 6px; }
      .product-main-divider span { right: 20px; }

      .special-product { padding: 110px 0; }

      .special-head { gap: 60px; }

      .special-head > h2 {
        font-size: clamp(58px, 17vw, 95px);
        letter-spacing: -4px;
      }

      .fire-test { margin-top: 90px; }
      .fire-test-image { height: 500px; }

      .fire-products { grid-template-columns: 1fr; }

      .fire-product {
        border-right: none;
        border-bottom: 1px solid #333;
      }

      .fire-product:last-child { border-bottom: none; }
      .fire-product-image { height: 350px; }


      /* PRODUCT 01~04 H/F */
      .product-profile-area.product-profile-hf {
        grid-template-columns: 1fr;
        gap: 45px;
      }

      .profile-variants {
        grid-template-columns: 1fr;
      }

      .profile-variant {
        padding: 40px 0;
      }

      .profile-variant + .profile-variant {
        border-left: none;
        border-top: 1px solid #d2d2ce;
      }

      .profile-variant-image {
        height: 330px;
      }

      .variant-width strong {
        font-size: 38px;
      }


    }

  </style>
</head>


<body>


  <!-- ======================================================
       01 / INTRO
  ======================================================= -->

  <section class="mpvc-intro">

    <div class="mpvc-inner">

      <div class="mpvc-label">
        MICROCELLULAR PVC SYSTEM
      </div>

      <h1 class="mpvc-title">
        M<span>-</span>PVC
      </h1>

      <h2 class="mpvc-headline">
        <strong>알루미늄의 강성</strong>과
        <strong>PVC의 단열성</strong>을 결합한<br />
        차세대 창호용 복합 프로파일
      </h2>


      <div class="mpvc-description-wrap">

        <div>

          <div class="mpvc-section-label">
            01 / WHAT IS M-PVC?
          </div>

          <img
            src="images/mpvc-profile.png"
            alt="M-PVC 프로파일"
            class="mpvc-description-image"
          />

        </div>


        <p class="mpvc-description">

          M-PVC는 modified pvc가 아닌
          <strong>Microcellular PVC 즉 미세기포PVC</strong>를 기반으로,
          알루미늄과 PVC를 하나의 프로파일로 결합한
          복합 창호 시스템입니다.

          <br /><br />

          알루미늄 프레임에
          <strong>PVC를 분사하여</strong> 우수한 기술력을 통해
          구조적으로 하나의 프레임을 만들었습니다.

          <br /><br />

          알루미늄이 가진
          <strong>구조적 강성과 정밀성</strong>,
          PVC가 가진
          <strong>우수한 단열 성능</strong>을 함께 활용해
          기존 창호 소재의 한계를 보완하도록
          설계되었습니다.

        </p>

      </div>

    </div>

    <div class="mpvc-side-text">
      바튼창호
    </div>

    <div class="scroll-down">
      SCROLL TO DISCOVER
      <span></span>
    </div>

  </section>



  <!-- ======================================================
       02 / WHY M-PVC
  ======================================================= -->

  <section class="mpvc-compare">

    <div class="compare-inner">

      <div class="compare-label">
        02 / WHY M-PVC
      </div>

      <div class="compare-head">

        <h2>
          왜 M-PVC인가?
        </h2>

        <p>
          창호 프로파일은 더 나은 단열성과
          구조적 안정성을 위해 계속 발전해왔습니다.

          <br /><br />

          <strong>M-PVC는</strong> 기존 PVC의 장점을 살리면서,
          미세발포 구조와 알루미늄을 결합해
          <strong>한 단계 더 높은 성능</strong>을 구현합니다.
        </p>

      </div>


      <div class="material-compare">

        <div class="material-card">

          <div class="material-top">
            <span>01</span>
            <span>BASIC</span>
          </div>

          <h3>U-PVC</h3>

          <div class="material-image">
            <img src="images/upvc.png" alt="U-PVC">
          </div>

          <div class="material-name">
            GENERAL STRUCTURE
          </div>

          <p>
            일반적인 PVC 구조로,
            PVC 고유의 단열성과 내식성을 활용한
            전통적인 창호 프로파일 소재입니다.
          </p>

        </div>


        <div class="material-card">

          <div class="material-top">
            <span>02</span>
            <span>NOW</span>
          </div>

          <h3>C-PVC</h3>

          <div class="material-image">
            <img src="images/cpvc.png" alt="C-PVC">
          </div>

          <div class="material-name">
            GENERAL STRUCTURE
          </div>

          <p>
            기존 PVC 대비 단열성과 소재 효율을
            향상시켜 알루미늄과 결합한 프로파일 구조입니다.
          </p>

        </div>


        <div class="material-card material-card-m">

          <div class="material-top">
            <span>03</span>
            <span>NEXT GENERATION</span>
          </div>

          <h3>M-PVC</h3>

          <div class="material-image">
            <img src="images/mpvc.png" alt="M-PVC">
          </div>

          <div class="material-name">
            MICROCELLULAR STRUCTURE
          </div>

          <p>
            더욱 미세하고 균일한 셀 구조의
            Microcellular PVC와 알루미늄을 결합해
            단열성과 구조적 강성을 함께 확보합니다.
          </p>

          <div class="mpvc-combination">
            <span>MICROCELLULAR PVC</span>
            <strong>+</strong>
            <span>ALUMINUM</span>
          </div>

        </div>

      </div>


      <div class="compare-table">

        <div class="compare-row compare-row-head">
          <div></div>
          <div>U-PVC</div>
          <div>C-PVC</div>
          <div class="highlight">M-PVC</div>
        </div>

        <div class="compare-row">
          <div class="compare-category">구조</div>
          <div>일반 U-PVC</div>
          <div>일반 C-PVC</div>
          <div class="highlight">미세기포 M-PVC</div>
        </div>

        <div class="compare-row">
          <div class="compare-category">PVC 구조</div>
          <div>U-PVC</div>
          <div>AL + C-PVC</div>
          <div class="highlight">AL + 미세기포 M-PVC</div>
        </div>

        <div class="compare-row">
          <div class="compare-category">알루미늄 복합</div>
          <div>YES</div>
          <div>YES</div>
          <div class="highlight">YES</div>
        </div>

        <div class="compare-row">
          <div class="compare-category">구조적 강성</div>
          <div>향상</div>
          <div>향상</div>
          <div class="highlight">극대화</div>
        </div>

        <div class="compare-row">
          <div class="compare-category">단열 성능</div>
          <div>GOOD</div>
          <div>BETTER</div>
          <div class="highlight">BEST</div>
        </div>

      </div>


      <div class="compare-final">

        <span>
          MICROCELLULAR STRUCTURE × ALUMINUM
        </span>

        <h3>
          기존 PVC의 장점은 살리고,<br />
          한계는 넘어섰습니다.
        </h3>

      </div>

    </div>

  </section>



  <!-- ======================================================
       03 / WHY BETTER
  ======================================================= -->

  <section class="mpvc-benefits">

    <div class="benefits-inner">

      <div class="benefits-label">
        03 / WHY BETTER
      </div>

      <div class="benefits-head">

        <h2>
          M-PVC의 <br>
          차이는 구조에서 <br>
         시작됩니다.
        </h2>

        <p>
          미세기포 구조의 M-PVC와 알루미늄을 결합하여
          단열부터 구조적 안정성까지,
          창호에 필요한 다양한 성능을 하나의 시스템에 담았습니다.
        </p>

      </div>


      <div class="benefits-grid">

        <div class="benefit-card">

          <div class="benefit-top">
            <span>01</span>
            <span>THERMAL INSULATION</span>
          </div>

          <div class="benefit-icon">
            <img src="images/thermal.png" alt="단열성">
          </div>

          <div class="benefit-content">

            <div class="benefit-en">
              HIGH INSULATION
            </div>

            <h3>단열성</h3>

            <p>
              미세하고 균일한 셀 구조가 열의 전달을 줄여
              높은 단열 성능을 구현하도록 설계되었습니다.
            </p>

          </div>

        </div>


        <div class="benefit-card">

          <div class="benefit-top">
            <span>02</span>
            <span>STRUCTURAL STRENGTH</span>
          </div>

          <div class="benefit-icon">
            <img src="images/strength.png" alt="구조적 강성">
          </div>

          <div class="benefit-content">

            <div class="benefit-en">
              HIGH STRENGTH
            </div>

            <h3>구조적 강성</h3>

            <p>
              알루미늄 프레임과 M-PVC를 구조적으로 결합하여
              안정적인 프레임 강성을 확보합니다.
            </p>

          </div>

        </div>


        <div class="benefit-card">

          <div class="benefit-top">
            <span>03</span>
            <span>SOUND INSULATION</span>
          </div>

          <div class="benefit-icon">
            <img src="images/sound.png" alt="방음성">
          </div>

          <div class="benefit-content">

            <div class="benefit-en">
              SOUND INSULATION
            </div>

            <h3>방음성</h3>

            <p>
              복합 프레임 구조를 통해 외부에서 전달되는 소음을 줄여
              보다 쾌적한 실내 환경을 만듭니다.
            </p>

          </div>

        </div>


        <div class="benefit-card">

          <div class="benefit-top">
            <span>04</span>
            <span>AIR · WATER · WIND</span>
          </div>

          <div class="benefit-icon">
            <img src="images/tightness.png" alt="기밀 수밀 방풍">
          </div>

          <div class="benefit-content">

            <div class="benefit-en">
              TIGHTNESS PERFORMANCE
            </div>

            <h3>기밀 · 수밀 · 방풍</h3>

            <p>
              정밀하게 결합된 프레임 구조를 통해 공기와 물의 침투를 줄이고,
              외부 풍압에 안정적으로 대응합니다.
            </p>

          </div>

        </div>


        <div class="benefit-card benefit-card-wide">

          <div class="benefit-top">
            <span>05</span>
            <span>SLIM FRAME</span>
          </div>

          <div class="benefit-icon">
            <img src="images/slim.png" alt="슬림 프레임">
          </div>

          <div class="benefit-content">

            <div class="benefit-en">
              SLIM DESIGN
            </div>

            <h3>슬림한 프레임</h3>

            <p>
              구조적 강성을 확보하면서 프레임을 보다 슬림하게 설계하여
              넓은 개방감과 세련된 외관을 구현합니다.
            </p>

          </div>

        </div>

      </div>

    </div>

  </section>



  <!-- ======================================================
       04 / M-PVC STRUCTURE
  ======================================================= -->

  <section class="mpvc-structure">

    <div class="structure-inner">

      <div class="structure-label">
        04 / M-PVC STRUCTURE
      </div>

      <div class="structure-head">

        <h2>
          하나의 기술,<br />
          두 가지 구조.
        </h2>

        <p>
          M-PVC는 적용 방식에 따라
          H TYPE과 F TYPE 두 가지 시스템으로 구성됩니다.

          <br /><br />

          적용 범위와 목적에 따라
          구조와 단열 성능에 최적화된 시스템을 선택할 수 있습니다.
        </p>

      </div>


      <div class="structure-types">

        <div class="structure-type">

          <div class="structure-type-top">
            <span>01</span>
            <span>HALF SYSTEM</span>
          </div>

          <h3>
            H
            <span>HALF TYPE</span>
          </h3>

          <div class="structure-profile">
            <img src="images/H.png" alt="M-PVC H TYPE">
          </div>

          <div class="structure-info">

            <div class="structure-info-label">
              M-PVC H TYPE
            </div>

            <h4>
              성능과 디자인의 균형
            </h4>

            <p>
              M-PVC H는 필요한 영역에 M-PVC를 적용하여
              알루미늄의 구조적 강성과 M-PVC의 단열 성능을
              균형 있게 활용하는 시스템입니다.
            </p>

          </div>

        </div>


        <div class="structure-type">

          <div class="structure-type-top">
            <span>02</span>
            <span>FULL SYSTEM</span>
          </div>

          <h3>
            F
            <span>FULL TYPE</span>
          </h3>

          <div class="structure-profile">
            <img src="images/F.png" alt="M-PVC F TYPE">
          </div>

          <div class="structure-info">

            <div class="structure-info-label">
              M-PVC F TYPE
            </div>

            <h4>
              단열 성능에 집중한 구조
            </h4>

            <p>
              M-PVC F는 M-PVC의 적용 범위를 확대하여
              열의 이동 경로를 더욱 효과적으로 차단하고,
              높은 단열 성능을 목표로 설계된 시스템입니다.
            </p>

          </div>

        </div>

      </div>


      <div class="structure-bottom">

        <div>

          <div class="structure-bottom-small">
            ALUMINUM × MICROCELLULAR PVC
          </div>

          <h3>
            목적은 달라도,<br />
            핵심 기술은 같습니다.
          </h3>

        </div>


        <p>
          H TYPE과 F TYPE 모두 알루미늄의 구조적 안정성과
          Microcellular PVC의 단열 특성을 결합합니다.

          적용 환경과 요구 성능에 따라 적합한 구조를 선택하여
          다양한 건축 환경에 대응할 수 있습니다.
        </p>

      </div>

    </div>

  </section>



  <!-- ======================================================
       05 / PERFORMANCE
  ======================================================= -->

  <section class="mpvc-performance">

    <div class="performance-inner">

      <div class="performance-label">
        05 / PERFORMANCE
      </div>


      <div class="performance-head">

        <h2>
          수치로 확인하는<br>
          M-PVC의 성능.
        </h2>

        <p>
          M-PVC는 단열, 차음, 결로방지 성능을 통해
          쾌적한 실내 환경을 위한
          창호 성능을 구현합니다.
        </p>

      </div>



      <!-- 01 열관류율 -->

      <div class="performance-block">

        <div class="performance-number-wrap">

          <div class="performance-index">
            THERMAL PERFORMANCE
          </div>

          <div class="performance-big-number">
            0.725
            <span>~</span>
            0.799
          </div>

          <div class="performance-unit">
            W/㎡·K
          </div>

        </div>


        <div class="performance-info">

          <div class="performance-en">
            THERMAL TRANSMITTANCE
          </div>

          <h3>
            열관류율
          </h3>

          <p>
            열관류율은 창호를 통해 전달되는
            열의 양을 나타내는 수치입니다.
            수치가 낮을수록 단열 성능이 우수합니다.
          </p>

        </div>

      </div>



      <!-- 02 차음 -->

      <div class="performance-block performance-block-reverse">

        <div class="performance-info">

          <div class="performance-en">
            SOUND INSULATION
          </div>

          <h3>
            차음성능
          </h3>

          <p>
            외부에서 발생하는 소음의 실내 유입을 줄여
            보다 조용하고 쾌적한
            실내 환경을 구현합니다.
          </p>

        </div>


        <div class="performance-number-wrap">

          <div class="performance-index">
            SOUND INSULATION
          </div>

          <div class="performance-big-number">
            40
            <span>~</span>
            45
          </div>

          <div class="performance-unit">
            dB
          </div>

        </div>

      </div>



      <!-- 03 결로 -->

      <div class="performance-condensation">

        <div class="condensation-top">

          <div>

            <div class="performance-index">
              CONDENSATION RESISTANCE
            </div>

            <h3>
              중부 1지역<br>
              기준 충족<br>
              전 지역 시공가능
            </h3>

          </div>


          <div>

            <div class="performance-en">
              CONDENSATION PERFORMANCE
            </div>

            <h4>
              결로방지성능
            </h4>

            <p>
              중부 1지역의 결로방지 성능기준을 기준으로
              유리 중앙부위, 모서리부위,
              창틀 및 창짝의 성능을 확보합니다.
            </p>

          </div>

        </div>


        <div class="condensation-values">

          <div class="condensation-item">

            <div class="condensation-name">
              유리 중앙부위
            </div>

            <div class="condensation-number">
              ≤ 0.16
            </div>

          </div>


          <div class="condensation-item">

            <div class="condensation-name">
              유리 모서리부위
            </div>

            <div class="condensation-number">
              ≤ 0.22
            </div>

          </div>


          <div class="condensation-item">

            <div class="condensation-name">
              창틀 및 창짝
            </div>

            <div class="condensation-number">
              ≤ 0.25
            </div>

          </div>

        </div>


        <div class="condensation-bottom">

          <span>
            중부 1지역 충족
          </span>

          <strong>
            전국 적용 가능 수준의 결로방지 성능
          </strong>

        </div>

      </div>


    </div>

  </section>



  <!-- ======================================================
       06 / PRODUCT LINE-UP
  ======================================================= -->

  <section class="mpvc-products">

    <div class="products-intro">
      <div class="products-inner">

        <div class="products-label">
          06 / PRODUCT LINE-UP
        </div>

        <div class="products-head">
          <h2>
            M-PVC,<br>
            다양한 <br>시스템창호로<br>
            완성됩니다.
          </h2>

          <p>
            M-PVC는 다양한 개폐 방식과 설계 조건에 맞춰
            여러 형태의 창호 시스템으로 구성됩니다.
            <br><br>
            프로파일 구조부터 적용 모습까지,
            M-PVC의 다양한 제품군을 확인해보세요.
          </p>
        </div>

      </div>
    </div>

    <!-- PRODUCT 01 / SYSTEM DOOR -->
    <article class="product-section product-light">
      <div class="product-inner">

        <div class="product-header">
          <div class="product-number">
            <span>PRODUCT</span>
            <strong>01</strong>
          </div>

          <div class="product-type">
            <span>M-PVC SYSTEM</span>
            <strong>SYSTEM DOOR</strong>
          </div>
        </div>

        <div class="product-profile-area product-profile-hf">
          <div class="product-profile-title">
            <span>PROFILE</span>
            <h3>시스템도어</h3>
          </div>

          <div class="profile-variants">

            <div class="profile-variant">
              <div class="profile-variant-image">
                <img src="images/system-door-h.png" alt="M-PVC 시스템도어 H TYPE">
              </div>

              <div class="profile-variant-info">
                <div class="variant-type">H TYPE</div>
                <div class="variant-width-label">FRAME WIDTH</div>
                <div class="variant-width">
                  <strong>096</strong>
                  <span>mm</span>
                </div>
              </div>
            </div>

            <div class="profile-variant">
              <div class="profile-variant-image">
                <img src="images/system-door-f.png" alt="M-PVC 시스템도어 F TYPE">
              </div>

              <div class="profile-variant-info">
                <div class="variant-type">F TYPE</div>
                <div class="variant-width-label">FRAME WIDTH</div>
                <div class="variant-width">
                  <strong>075</strong>
                  <span>mm</span>
                </div>
              </div>
            </div>

          </div>
        </div>

        <div class="product-inner-divider"></div>

        <div class="product-application">
          <div class="application-head">
            <div>
              <span>APPLICATION</span>
              <h3>시스템도어 적용 모습</h3>
            </div>

            <p>
              바튼창호의 시스템창호가 건축 공간에
              적용된 모습입니다.
            </p>
          </div>

          <div class="application-image">
            <img src="images/system-door-install.jpg" alt="M-PVC 시스템도어 시공사진">
          </div>
        </div>

      </div>
    </article>

    <div class="product-main-divider">
      <span>NEXT PRODUCT / 02</span>
    </div>

    <!-- PRODUCT 02 / CASEMENT -->
    <article class="product-section product-white">
      <div class="product-inner">

        <div class="product-header">
          <div class="product-number">
            <span>PRODUCT</span>
            <strong>02</strong>
          </div>

          <div class="product-type">
            <span>M-PVC SYSTEM</span>
            <strong>CASEMENT</strong>
          </div>
        </div>

        <div class="product-profile-area product-profile-hf">
          <div class="product-profile-title">
            <span>PROFILE</span>
            <h3>케이스먼트</h3>
          </div>

          <div class="profile-variants">

            <div class="profile-variant">
              <div class="profile-variant-image">
                <img src="images/casement-h.png" alt="M-PVC 케이스먼트 H TYPE">
              </div>

              <div class="profile-variant-info">
                <div class="variant-type">H TYPE</div>
                <div class="variant-width-label">FRAME WIDTH</div>
                <div class="variant-width">
                  <strong>074</strong>
                  <span>mm</span>
                </div>
              </div>
            </div>

            <div class="profile-variant">
              <div class="profile-variant-image">
                <img src="images/casement-f.png" alt="M-PVC 케이스먼트 F TYPE">
              </div>

              <div class="profile-variant-info">
                <div class="variant-type">F TYPE</div>
                <div class="variant-width-label">FRAME WIDTH</div>
                <div class="variant-width">
                  <strong>075</strong>
                  <span>mm</span>
                </div>
              </div>
            </div>

          </div>
        </div>

        <div class="product-inner-divider"></div>

        <div class="product-application">
          <div class="application-head">
            <div>
              <span>APPLICATION</span>
              <h3>케이스먼트 적용 모습</h3>
            </div>

            <p>
              바튼창호의 시스템창호가 건축 공간에
              적용된 모습입니다.
            </p>
          </div>

          <div class="application-image">
            <img src="images/casement-install.jpg" alt="M-PVC 케이스먼트 시공사진">
          </div>
        </div>

      </div>
    </article>

    <div class="product-main-divider">
      <span>NEXT PRODUCT / 03</span>
    </div>

    <!-- PRODUCT 03 / PROJECT WINDOW -->
    <article class="product-section product-light">
      <div class="product-inner">

        <div class="product-header">
          <div class="product-number">
            <span>PRODUCT</span>
            <strong>03</strong>
          </div>

          <div class="product-type">
            <span>M-PVC SYSTEM</span>
            <strong>PROJECT WINDOW</strong>
          </div>
        </div>

        <div class="product-profile-area product-profile-hf">
          <div class="product-profile-title">
            <span>PROFILE</span>
            <h3>프로젝트</h3>
          </div>

          <div class="profile-variants">

            <div class="profile-variant">
              <div class="profile-variant-image">
                <img src="images/project-h.png" alt="M-PVC 프로젝트 H TYPE">
              </div>

              <div class="profile-variant-info">
                <div class="variant-type">H TYPE</div>
                <div class="variant-width-label">FRAME WIDTH</div>
                <div class="variant-width">
                  <strong>074</strong>
                  <span>mm</span>
                </div>
              </div>
            </div>

            <div class="profile-variant">
              <div class="profile-variant-image">
                <img src="images/project-f.png" alt="M-PVC 프로젝트 F TYPE">
              </div>

              <div class="profile-variant-info">
                <div class="variant-type">F TYPE</div>
                <div class="variant-width-label">FRAME WIDTH</div>
                <div class="variant-width">
                  <strong>075</strong>
                  <span>mm</span>
                </div>
              </div>
            </div>

          </div>
        </div>

        <div class="product-inner-divider"></div>

        <div class="product-application">
          <div class="application-head">
            <div>
              <span>APPLICATION</span>
              <h3>프로젝트 적용 모습</h3>
            </div>

            <p>
              바튼창호의 시스템창호가 건축 공간에
              적용된 모습입니다.
            </p>
          </div>

          <div class="application-image">
            <img src="images/project-install.jpg" alt="M-PVC 프로젝트 시공사진">
          </div>
        </div>

      </div>
    </article>

    <div class="product-main-divider">
      <span>NEXT PRODUCT / 04</span>
    </div>

    <!-- PRODUCT 04 / TILT & TURN -->
    <article class="product-section product-white">
      <div class="product-inner">

        <div class="product-header">
          <div class="product-number">
            <span>PRODUCT</span>
            <strong>04</strong>
          </div>

          <div class="product-type">
            <span>M-PVC SYSTEM</span>
            <strong>TILT &amp; TURN</strong>
          </div>
        </div>

        <div class="product-profile-area product-profile-hf">
          <div class="product-profile-title">
            <span>PROFILE</span>
            <h3>틸트 &amp; 턴</h3>
          </div>

          <div class="profile-variants">

            <div class="profile-variant">
              <div class="profile-variant-image">
                <img src="images/tilt-turn-h.png" alt="M-PVC 틸트 &amp; 턴 H TYPE">
              </div>

              <div class="profile-variant-info">
                <div class="variant-type">H TYPE</div>
                <div class="variant-width-label">FRAME WIDTH</div>
                <div class="variant-width">
                  <strong>080</strong>
                  <span>mm</span>
                </div>
              </div>
            </div>

            <div class="profile-variant">
              <div class="profile-variant-image">
                <img src="images/tilt-turn-f.png" alt="M-PVC 틸트 &amp; 턴 F TYPE">
              </div>

              <div class="profile-variant-info">
                <div class="variant-type">F TYPE</div>
                <div class="variant-width-label">FRAME WIDTH</div>
                <div class="variant-width">
                  <strong>090</strong>
                  <span>mm</span>
                </div>
              </div>
            </div>

          </div>
        </div>

        <div class="product-inner-divider"></div>

        <div class="product-application">
          <div class="application-head">
            <div>
              <span>APPLICATION</span>
              <h3>틸트 &amp; 턴 적용 모습</h3>
            </div>

            <p>
              바튼창호의 시스템창호가 건축 공간에
              적용된 모습입니다.
            </p>
          </div>

          <div class="application-image">
            <img src="images/tilt-turn-install.jpg" alt="M-PVC 틸트 &amp; 턴 시공사진">
          </div>
        </div>

      </div>
    </article>

    <div class="product-main-divider">
      <span>NEXT PRODUCT / 05</span>
    </div>

    <!-- PRODUCT 05 / PARALLEL SLIDING -->
    <article class="product-section product-light">
      <div class="product-inner">

        <div class="product-header">
          <div class="product-number">
            <span>PRODUCT</span>
            <strong>05</strong>
          </div>

          <div class="product-type">
            <span>M-PVC SYSTEM</span>
            <strong>PARALLEL SLIDING</strong>
          </div>
        </div>

        <div class="product-profile-area">
          <div class="product-profile-title">
            <span>PROFILE</span>
            <h3>수평밀착 슬라이딩</h3>
          </div>

          <div class="product-profile-image">
            <img src="images/parallel-sliding.png" alt="M-PVC 수평밀착 슬라이딩 프로파일">
          </div>

          <div class="product-size">
            <span>FRAME WIDTH</span>
            <div class="product-size-value">
              <strong>141</strong>
              <em>mm</em>
            </div>
          </div>
        </div>

        <div class="product-inner-divider"></div>

        <div class="product-application">
          <div class="application-head">
            <div>
              <span>APPLICATION</span>
              <h3>수평밀착 슬라이딩 적용 모습</h3>
            </div>

            <p>
              바튼창호의 시스템창호가 건축 공간에
              적용된 모습입니다.
            </p>
          </div>

          <div class="application-image">
            <img src="images/parallel-sliding-install.jpg" alt="M-PVC 수평밀착 슬라이딩 시공사진">
          </div>
        </div>

      </div>
    </article>

    <div class="product-main-divider">
      <span>NEXT PRODUCT / 06</span>
    </div>

    <!-- PRODUCT 06 / TILT & SLIDE -->
    <article class="product-section product-white">
      <div class="product-inner">

        <div class="product-header">
          <div class="product-number">
            <span>PRODUCT</span>
            <strong>06</strong>
          </div>

          <div class="product-type">
            <span>M-PVC SYSTEM</span>
            <strong>TILT &amp; SLIDE</strong>
          </div>
        </div>

        <div class="product-profile-area">
          <div class="product-profile-title">
            <span>PROFILE</span>
            <h3>틸트 &amp; 슬라이딩</h3>
          </div>

          <div class="product-profile-image">
            <img src="images/tilt-slide.png" alt="M-PVC 틸트 &amp; 슬라이딩 프로파일">
          </div>

          <div class="product-size">
            <span>FRAME WIDTH</span>
            <div class="product-size-value">
              <strong>095</strong>
              <em>mm</em>
            </div>
          </div>
        </div>

        <div class="product-inner-divider"></div>

        <div class="product-application">
          <div class="application-head">
            <div>
              <span>APPLICATION</span>
              <h3>틸트 &amp; 슬라이딩 적용 모습</h3>
            </div>

            <p>
             바튼창호의 시스템창호가 건축 공간에
              적용된 모습입니다.
            </p>
          </div>

          <div class="application-image">
            <img src="images/tilt-slide-install.png" alt="M-PVC 틸트 &amp; 슬라이딩 시공사진">
          </div>
        </div>

      </div>
    </article>

    <!-- SPECIAL PRODUCT / FIRE RESISTANT WINDOW -->
    <section class="special-product">
      <div class="special-inner">

        <div class="special-label">
          SPECIAL PRODUCT
        </div>

        <div class="special-head">
          <h2>
            FIRE RESISTANT<br>
            WINDOW
          </h2>

          <div class="special-description">
            <span>M-PVC SPECIAL SYSTEM</span>

            <h3>
              방화 성능을 더한<br>
              바튼창호의 시스템 방화창.
            </h3>

            <p>
              방화 성능이 요구되는 건축 환경을 위한
              바튼창호의 특수 시스템창호입니다.
            </p>
          </div>
        </div>

        <div class="fire-test">
          <div class="fire-test-head">
            <div>
              <span>FIRE RESISTANCE TEST</span>
              <h3>방화 성능 시험 - 비차열 20분 통과</h3>
            </div>

            <div class="fire-test-number">TEST</div>
          </div>

          <div class="fire-test-image">
            <img src="images/fire-test.jpg" alt="M-PVC 방화창 방화시험">
          </div>
        </div>

        <div class="fire-lineup">
          <div class="fire-lineup-head">
            <span>FIRE WINDOW LINE-UP</span>
            <h3>방화창 제품군</h3>
          </div>

          <div class="fire-products">

            <div class="fire-product">
              <div class="fire-product-number">01</div>
              <div class="fire-product-image">
                <img src="images/fire01.png" alt="M-PVC 방화창 제품 01">
              </div>
              <div class="fire-product-info">
                <span>FIRE WINDOW</span>
                <h4>방화 수평밀착 슬라이딩</h4>
                <div class="fire-size">
                  <span>FRAME WIDTH</span>
                  <strong>153</strong><em>mm</em>
                </div>
              </div>
            </div>

            <div class="fire-product">
              <div class="fire-product-number">02</div>
              <div class="fire-product-image">
                <img src="images/fire02.png" alt="M-PVC 방화창 제품 02">
              </div>
              <div class="fire-product-info">
                <span>FIRE WINDOW</span>
                <h4>방화 틸트&턴</h4>
                <div class="fire-size">
                  <span>FRAME WIDTH</span>
                  <strong>090</strong><em>mm</em>
                </div>
              </div>
            </div>

            <div class="fire-product">
              <div class="fire-product-number">03</div>
              <div class="fire-product-image">
                <img src="images/fire03.png" alt="M-PVC 방화창 제품 03">
              </div>
              <div class="fire-product-info">
                <span>FIRE WINDOW</span>
                <h4>방화 프로젝트</h4>
                <div class="fire-size">
                  <span>FRAME WIDTH</span>
                  <strong>080</strong><em>mm</em>
                </div>
              </div>
            </div>

          </div>
        </div>

      </div>
    </section>

  </section>

  <img width="383" height="487" alt="Image" src="https://github.com/user-attachments/assets/e03770b1-24b3-4e62-8223-7eecd80182f9" />
<img width="375" height="478" alt="Image" src="https://github.com/user-attachments/assets/d22cdbe8-49b2-4d39-9302-d13af46662cc" />
<img width="966" height="644" alt="Image" src="https://github.com/user-attachments/assets/1d965126-2b89-46a8-a99c-ba2175b22147" />
<img width="1933" height="1892" alt="Image" src="https://github.com/user-attachments/assets/73b0d73c-3e38-44ed-befa-d371b2d6a3dc" />
<img width="1728" height="2160" alt="Image" src="https://github.com/user-attachments/assets/0d145bd7-6b5d-425d-80c2-75f9a5ae10af" />
<img width="860" height="700" alt="Image" src="https://github.com/user-attachments/assets/58ac43cc-4b84-4aa6-9b22-9a119a05ebd7" />
<img width="466" height="607" alt="Image" src="https://github.com/user-attachments/assets/e0aaccaf-d125-4bd0-b5a7-cbc088bc5ec7" />
<img width="966" height="644" alt="Image" src="https://github.com/user-attachments/assets/891cd4db-f74f-4a39-91e0-ab991902ab9d" />
<img width="2826" height="2185" alt="Image" src="https://github.com/user-attachments/assets/4743f2a3-09eb-41fa-91c3-76ec2ec07623" />
<img width="390" height="639" alt="Image" src="https://github.com/user-attachments/assets/e89641cf-fc28-4b69-a969-c48c01af910b" />
<img width="363" height="648" alt="Image" src="https://github.com/user-attachments/assets/a9604527-6b43-407c-983e-a64692a27a3a" />
<img width="966" height="677" alt="Image" src="https://github.com/user-attachments/assets/35a7390d-92ab-4360-844d-908db5267968" />
<img width="1536" height="1024" alt="Image" src="https://github.com/user-attachments/assets/9ba37a21-dd1d-4d41-be3f-7c177b40bfd5" />
<img width="1536" height="1024" alt="Image" src="https://github.com/user-attachments/assets/3319c7cc-e6df-419b-941d-ea5bb6a27e1e" />
<img width="1254" height="1254" alt="Image" src="https://github.com/user-attachments/assets/432d5ff3-4316-48fd-882f-b69c5124a038" />
<img width="2783" height="2185" alt="Image" src="https://github.com/user-attachments/assets/ef931cf0-631e-4fd1-adf5-a5b0e8f727d8" />
<img width="404" height="632" alt="Image" src="https://github.com/user-attachments/assets/43fea814-fc9e-4d92-8787-c1a61ee77246" />
<img width="387" height="640" alt="Image" src="https://github.com/user-attachments/assets/ab7faaaf-ba5f-4b62-93a6-b45d5f3007a2" />
<img width="966" height="644" alt="Image" src="https://github.com/user-attachments/assets/eb0bf526-ae03-4f85-9325-94be76f6da2a" />
<img width="1254" height="1254" alt="Image" src="https://github.com/user-attachments/assets/2638f33f-4484-4d3c-8b56-233fd2178986" />
<img width="1536" height="1024" alt="Image" src="https://github.com/user-attachments/assets/8f8a2c83-c79d-4472-a35b-93430603e4d3" />
<img width="383" height="635" alt="Image" src="https://github.com/user-attachments/assets/7897eaf3-4a42-41b6-a61a-5c66c18095f7" />
<img width="1492" height="1054" alt="Image" src="https://github.com/user-attachments/assets/8a62bb30-3535-49bc-9662-ad135d0e859b" />
<img width="2826" height="2185" alt="Image" src="https://github.com/user-attachments/assets/105d967a-2f64-4671-9c24-936edcf614d2" />
<img width="392" height="636" alt="Image" src="https://github.com/user-attachments/assets/e93e83d8-3623-4a11-af7a-174095f52db6" />
<img width="366" height="636" alt="Image" src="https://github.com/user-attachments/assets/a2fe1fc2-446d-4df5-a69a-750ac29d330b" />
<img width="966" height="644" alt="Image" src="https://github.com/user-attachments/assets/688bfce1-a7d8-4202-83e4-fca9b35f83a8" />
<img width="314" height="480" alt="Image" src="https://github.com/user-attachments/assets/4688d5d9-dfbf-442b-9627-15cec66358aa" />
<img width="2826" height="2185" alt="Image" src="https://github.com/user-attachments/assets/9e994351-2f11-4ed2-b0b6-305267d2f1a4" />
<img width="393" height="636" alt="Image" src="https://github.com/user-attachments/assets/03f83e8a-a6d9-4a3c-92d6-01b6218711d4" />
<img width="366" height="635" alt="Image" src="https://github.com/user-attachments/assets/ac138b3b-6694-41c1-a388-2e045877d783" />
<img width="966" height="644" alt="Image" src="https://github.com/user-attachments/assets/f92c140c-990a-405d-b9b7-7cb703f16791" />
<img width="2071" height="2160" alt="Image" src="https://github.com/user-attachments/assets/eb76e688-3d5e-48c1-8c8e-3b48f7b3199b" />
<img width="1989" height="1907" alt="Image" src="https://github.com/user-attachments/assets/1dc4fb98-fb6f-4aad-b959-6276bc905a35" />
<img width="1535" height="1024" alt="Image" src="https://github.com/user-attachments/assets/31e7c60b-27e0-49e6-87f6-e47dc7983ff2" />
<img width="450" height="496" alt="Image" src="https://github.com/user-attachments/assets/d64d89f5-9950-406f-a54a-bc68efb07985" />


</body>
</html>
