<template>
  <section class="section section_how-works">
    <div class="container">
      <hgroup class="text-center">
        <h2>
          How we works ?
        </h2>
        <p>
          This is a process, how you can get loan for your self.
        </p>
      </hgroup>

      <div class="">
        <div class="row_2" v-for="(item, ind) in str" :key="ind">
          <div>
            <img :src="item.img" alt="item.title" />
          </div>
          <div class="row_2-col">
            <h3>{{ item.title }}</h3>
            <div>
              {{ item.desc }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import img1 from "~/assets/img/img2.svg";
import img2 from "~/assets/img/img3.svg";
import img3 from "~/assets/img/img4.svg";
import img4 from "~/assets/img/img5.svg";

const str = [
  {
    title: "Application",
    desc:
      "The borrower submits a loan application to the bank, either in person, online, or through other channels. The application includes personal and financial information, such as income, employment history, credit score, and the purpose of the loan.",
    img: img1,
  },
  {
    title: "Documentation and Verification",
    desc:
      "The bank requests supporting documents from the borrower, such as identification proof, income statements, bank statements, and collateral details (if applicable). The bank verifies the information provided to assess the borrower's creditworthiness and eligibility for the loan.",
    img: img2,
  },
  {
    title: "Credit Assessment",
    desc:
      "The bank conducts a credit assessment to evaluate the borrower's creditworthiness and ability to repay the loan. This process involves analyzing the borrower's credit history, income stability, debt-to-income ratio, and other factors.",
    img: img3,
  },
  {
    title: "Loan Approval",
    desc:
      "If the borrower meets the bank's lending criteria and passes the credit assessment, the loan is approved. The bank determines the loan amount, interest rate, repayment term, and any associated fees.",
    img: img4,
  },
];
</script>
