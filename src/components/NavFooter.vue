<template>
    <section class="flex flex-col justify-start pt-16 mx-5">
            <!-- Logo dulu -->
            <a href="#" class="flex items-center bg-green-600 px-1 lg:px-2 py-1.5 lg:py-2.5 rounded w-fit mb-8">
              <img src="/public/aej-logo.svg" class="h-7" alt="AEJ Logo" />
            </a>
            <div>
                <div class="hidden sm:grid grid-cols-5 gap-5 grid-flow-row place-content-around justify-center">
                    <div class="mx-4 mt-3">
                        <h1 class="font-semibold">Featured Programs</h1>
                        <ul class="mt-4">
                            <li class="text-sm font-light ml-3 mt-2">Business Analytics</li>
                            <li class="text-sm font-light ml-3 mt-2">SQL</li>
                            <li class="text-sm font-light ml-3 mt-2">Data Engineering with AWS</li>
                            <li class="text-sm font-light ml-3 mt-2">Data Analyst</li>
                            <li class="text-sm font-light ml-3 mt-2">Intro to Programming</li>
                            <li class="text-sm font-light ml-3 mt-2">Digital Marketing</li>
                            <li class="text-sm font-light ml-3 mt-2">Self Driving Car Engineer</li>
                        </ul>
                    </div>
                    <div class="mx-4 mt-3">
                        <h1 class="font-semibold">Only At AEJ</h1>
                        <ul class="mt-4">
                            <li class="text-sm font-light ml-3 mt-2">Artificial Intelligence</li>
                            <li class="text-sm font-light ml-3 mt-2">Deep Learning</li>
                            <li class="text-sm font-light ml-3 mt-2">Digital Marketing</li>
                            <li class="text-sm font-light ml-3 mt-2">Flying Car and Autonomous Flight Engineer</li>
                            <li class="text-sm font-light ml-3 mt-2">Intro to Self-Driving Cars</li>
                            <li class="text-sm font-light ml-3 mt-2">Machine Learning Engineer</li>
                            <li class="text-sm font-light ml-3 mt-2">Robotics Software Engineer</li>
                        </ul>
                    </div>
                    <div class="mx-4 mt-3">
                        <h1 class="font-semibold">Enterprise</h1>
                        <ul class="mt-4">
                            <li class="text-sm font-light ml-3 mt-2">Udacity for Enterprise</li>
                            <li class="text-sm font-light ml-3 mt-2">Digital Transformation with Udacity</li>
                            <li class="text-sm font-light ml-3 mt-2">Artificial Intelligence for Enterprise</li>
                            <li class="text-sm font-light ml-3 mt-2">Cybersecurity for Enterprise</li>
                            <li class="text-sm font-light ml-3 mt-2">Data Science for Enterprise</li>
                            <li class="text-sm font-light ml-3 mt-2">Udacity for Financial Services</li>
                            <li class="text-sm font-light ml-3 mt-2">Corporate Social Responsibility</li>
                            <li class="text-sm font-light ml-3 mt-2">Train-to-Hire</li>
                            <li class="text-sm font-light ml-3 mt-2">Enterprise Resource Center</li>
                        </ul>
                    </div>
                    <div class="mx-4 mt-3">
                        <h1 class="font-semibold">Resources</h1>
                        <ul class="mt-4">
                            <li class="text-sm font-light ml-3 mt-2">Catalog</li>
                            <li class="text-sm font-light ml-3 mt-2">Career Services</li>
                            <li class="text-sm font-light ml-3 mt-2">Student Success</li>
                            <li class="text-sm font-light ml-3 mt-2">Udacity Talks</li>
                            <li class="text-sm font-light ml-3 mt-2">Scholarships</li>
                            <li class="text-sm font-light ml-3 mt-2">What is AI?</li>
                        </ul>
                    </div>
                    <div class="mx-4 mt-3">
                        <h1 class="font-semibold">Support</h1>
                        <ul class="mt-4">
                            <li class="text-sm font-light ml-3 mt-2">Contact Us</li>
                            <li class="text-sm font-light ml-3 mt-2">Help and FAQ</li>
                            <li class="text-sm font-light ml-3 mt-2">Service Status</li>
                            <li class="text-sm font-light ml-3 mt-2">Tech Requirements</li>
                        </ul>
                    </div>
                    <div class="mx-4 mt-3">
                        <h1 class="font-semibold">AEJ Schools</h1>
                        <ul class="mt-4">
                            <li class="text-sm font-light ml-3 mt-2">School of Artificial Intelligence</li>
                            <li class="text-sm font-light ml-3 mt-2">School of Autonomous Systems</li>
                        </ul>
                    </div>
                    <div class="mx-4 mt-3">
                        <h1 class="font-semibold">Company</h1>
                        <ul class="mt-4">
                            <li class="text-sm font-light ml-3 mt-2">About</li>
                            <li class="text-sm font-light ml-3 mt-2">Blog</li>
                        </ul>
                    </div>
                    <div class="mx-4 mt-3">
                        <h1 class="font-semibold">Government</h1>
                        <ul class="mt-4">
                            <li class="text-sm font-light ml-3 mt-2">AEJ for Government</li>
                        </ul>
                    </div>
                
                </div>
                <Accordion :activeIndex="0" class="block sm:hidden">
                    <AccordionTab header="Featured Program">
                        <ul class="mt-4">
                            <li class="text-sm font-light ml-3 mt-2">Business Analytics</li>
                            <li class="text-sm font-light ml-3 mt-2">SQL</li>
                            <li class="text-sm font-light ml-3 mt-2">Data Engineering with AWS</li>
                            <li class="text-sm font-light ml-3 mt-2">Data Analyst</li>
                            <li class="text-sm font-light ml-3 mt-2">Intro to Programming</li>
                            <li class="text-sm font-light ml-3 mt-2">Digital Marketing</li>
                            <li class="text-sm font-light ml-3 mt-2">Self Driving Car Engineer</li>
                        </ul>
                    </AccordionTab>
                    <AccordionTab header="Only at AEJ">
                        <ul class="mt-4">
                            <li class="text-sm font-light ml-3 mt-2">Artificial Intelligence</li>
                            <li class="text-sm font-light ml-3 mt-2">Deep Learning</li>
                            <li class="text-sm font-light ml-3 mt-2">Digital Marketing</li>
                            <li class="text-sm font-light ml-3 mt-2">Flying Car and Autonomous Flight Engineer</li>
                            <li class="text-sm font-light ml-3 mt-2">Intro to Self-Driving Cars</li>
                            <li class="text-sm font-light ml-3 mt-2">Machine Learning Engineer</li>
                            <li class="text-sm font-light ml-3 mt-2">Robotics Software Engineer</li>
                        </ul>
                    </AccordionTab>
                    <AccordionTab header="Enterprise">
                        <ul class="mt-4">
                            <li class="text-sm font-light ml-3 mt-2">Udacity for Enterprise</li>
                            <li class="text-sm font-light ml-3 mt-2">Digital Transformation with Udacity</li>
                            <li class="text-sm font-light ml-3 mt-2">Artificial Intelligence for Enterprise</li>
                            <li class="text-sm font-light ml-3 mt-2">Cybersecurity for Enterprise</li>
                            <li class="text-sm font-light ml-3 mt-2">Data Science for Enterprise</li>
                            <li class="text-sm font-light ml-3 mt-2">Udacity for Financial Services</li>
                            <li class="text-sm font-light ml-3 mt-2">Corporate Social Responsibility</li>
                            <li class="text-sm font-light ml-3 mt-2">Train-to-Hire</li>
                            <li class="text-sm font-light ml-3 mt-2">Enterprise Resource Center</li>
                        </ul>
                    </AccordionTab>
                    <AccordionTab header="Resources">
                        <ul class="mt-4">
                            <li class="text-sm font-light ml-3 mt-2">Catalog</li>
                            <li class="text-sm font-light ml-3 mt-2">Career Services</li>
                            <li class="text-sm font-light ml-3 mt-2">Student Success</li>
                            <li class="text-sm font-light ml-3 mt-2">Udacity Talks</li>
                            <li class="text-sm font-light ml-3 mt-2">Scholarships</li>
                            <li class="text-sm font-light ml-3 mt-2">What is AI?</li>
                        </ul>
                    </AccordionTab>
                    <AccordionTab header="Supports">
                        <ul class="mt-4">
                            <li class="text-sm font-light ml-3 mt-2">Contact Us</li>
                            <li class="text-sm font-light ml-3 mt-2">Help and FAQ</li>
                            <li class="text-sm font-light ml-3 mt-2">Service Status</li>
                            <li class="text-sm font-light ml-3 mt-2">Tech Requirements</li>
                        </ul>
                    </AccordionTab>
                </Accordion>
            </div>
        </section>
</template>